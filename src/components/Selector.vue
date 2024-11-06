<script>
    export default {
        props: {
            setCrypto: {
                type: Function,
                required: true
            },
            cryptoNow: {
                type: String,
                required: true
            }
        },
        data() {
            return {
                current: ''
            }
        },
        methods: {
            selectItem(val) {
                this.setCrypto(val);
                this.current = val;
            }
        }
    }
</script>

<template>
    <ul>
        <li @click="selectItem('BTC')" :className="cryptoNow === 'BTC' ? 'active' : ''">Bitcoin</li>
        <li @click="selectItem('ETH')" :className="cryptoNow === 'ETH' ? 'active' : ''">Ethereum</li>
        <li @click="selectItem('USDT')" :className="cryptoNow === 'USDT' ? 'active' : ''">USDT</li>
    </ul>
</template>

<style scoped>
   ul {
    list-style: none;
    width: 200px;
    padding: 0;
    border-radius: 3px;
    border: 3px solid #000;
   }

   li {
    display: block;
    background: #540d8f;
    color: #fff;
    padding: 20px 0;
   }

   li:hover {
    background: #24043e;
    cursor: pointer;
   }

   li.active {
    background: #24043e;
   }

</style>