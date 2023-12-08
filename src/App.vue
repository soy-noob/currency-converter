<script>
import { onMounted } from 'vue'

onMounted

export default {
    methods: {
        Convert() {
            const currencyInput = document.querySelector('.currency-input')
            const convertLine = document.querySelector('.converted-line')
            convertLine.innerHTML = currencyInput.value * 0.1398
        }
    }
}
</script>

<template>
    <div class="container">
        <form>
            <div class="label">Currency Converter</div>
            <div class="currency-area">
                <div class="up-currency currency-box">
                    <div class="title">currency A</div>
                    <div class="country-box">
                        <div class="country-dropdown">
                            <p class="country-name">美国</p>
                            <img
                                class="dropdown-arrow"
                                src="./dropdown-arrow.svg"
                            />
                        </div>
                        <img src="./1x1/us.svg" class="country-logo" />
                        <div class="now-country">
                            <div class="country-name-EN">USD</div>
                            <div class="country-name-CN">美元</div>
                        </div>
                        <input
                            class="currency-input"
                            type="text"
                            placeholder="please type amount here"
                        />
                    </div>
                </div>
                <div class="swapBtn-area">
                    <div class="swapBtn">
                        <img src="./swap.svg" class="swapBtn-icon" />
                    </div>
                </div>
                <div class="below-currency currency-box">
                    <div class="title">currency B</div>
                    <div class="country-box">
                        <div class="country-dropdown">
                            <p class="country-name">中国</p>
                            <img
                                class="dropdown-arrow"
                                src="./dropdown-arrow.svg"
                            />
                        </div>
                        <img src="./1x1/cn.svg" class="country-logo" />
                        <div class="now-country">
                            <div class="country-name-EN">CNY</div>
                            <div class="country-name-CN">人民币</div>
                        </div>
                        <p class="converted-line"></p>
                    </div>
                </div>
            </div>
            <div class="convert-area">
                <div class="convert-button" @click="Convert">
                    <span>Convert</span>
                </div>
            </div>
        </form>
    </div>
</template>
