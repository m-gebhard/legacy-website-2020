<template>
    <div class="contact-box">
        <form class="contact-box__form"
              method="POST"
              action="https://formsubmit.co">
            <div class="contact-box__row">
                <div class="contact-box__input">
                    <label for="name">Name</label>
                    <div>
                        <input v-html="inputName"
                               id="name"
                               name="name"
                               autocomplete="given-name"
                               required
                               type="text">
                    </div>
                </div>
                <div class="contact-box__input">
                    <label for="email">Email</label>
                    <div>
                        <input v-html="inputEmail"
                               id="email"
                               name="email"
                               autocomplete="email"
                               required
                               type="email">
                    </div>
                </div>
            </div>
            <div class="contact-box__row">
                <div class="contact-box__input">
                    <label for="message">Message</label>
                    <div>
                        <textarea required
                                  name="message"
                                  id="message">
                        </textarea>
                    </div>
                </div>
            </div>
            <button class="contact-box__form-submit" type="submit">
                <span>Submit</span>
                <font-awesome-icon icon="paper-plane"></font-awesome-icon>
            </button>
        </form>
        <div class="contact-box__details">
            <h3>Say
                <span>Hello</span>
                !
            </h3>
            <p class="contact-box__details-info">
                Contact me and I’ll get back to you within a day.
            </p>
            <div class="contact-box__details-item">
                <span>Mannheim, <span>Germany</span></span>
                <font-awesome-icon icon="compass"></font-awesome-icon>
            </div>
            <div class="contact-box__details-item">
                <a href="mailto:contact@m-gebhard.dev">contact@m-gebhard.dev</a>
                <font-awesome-icon icon="at"></font-awesome-icon>
            </div>
        </div>
        <div class="contact-box__scroll-top">
            <scroll-top></scroll-top>
        </div>
    </div>
</template>

<script>
    import ScrollTop from './ScrollTop';

    export default {
        name:       'contact-box',
        components: { ScrollTop },
        data() {
            return {
                inputName:    '',
                inputEmail:   '',
                inputMessage: '',
            };
        },
    };
</script>
