<template>
  <v-container class="auth-form__container d-flex justify-center align-center">
    <div class="auth-form__border">
      <div class="auth-form__wrapper">
        <div class="auth-form__head mb-8">
          <div class="auth-form__title text-h4 text-center mb-2">Sign Up for Free</div>
          <div class="subtitle-1 text-center">Welcome, let’s get to know each other!</div>
        </div>

        <v-form class="mb-12">
          <div class="input-group">
            <div class="input-group__label">Full Name</div>
            <v-text-field
                v-model="fullName"
                placeholder="Enter your full name"
                class="input-group__input mb-5"
                dense
                hide-details
            ></v-text-field>
          </div>
          <div class="input-group">
            <div class="input-group__label">Email</div>
            <v-text-field
                v-model="email"
                placeholder="Enter your email"
                class="input-group__input mb-5"
                dense
                hide-details
            ></v-text-field>
          </div>
          <div class="input-group">
            <div class="input-group__label">Phone number</div>
            <v-text-field
                v-model="phone"
                placeholder="Enter your phone number"
                class="input-group__input mb-8"
                dense
                hide-details
            ></v-text-field>
          </div>

          <v-col cols="12" class="pa-0 mb-5">
            <v-btn
                class="btn-custom body-1"
                width="100%"
                min-height="52"
            >
              Continue
            </v-btn>
          </v-col>


          <v-col cols="12" class="pa-0">
            <v-btn
                class="btn-custom body-1 btn-t2"
                min-height="52"
                width="100%"
                dark
                outlined
            >
              I have an account
            </v-btn>
          </v-col>
        </v-form>
        <div class="auth-form__footer text-center text-caption">
          By signing up, you agree to the <a href="#">Terms of Service</a> and <a href="#">Privacy Policy</a>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      fullName: '',
      email: '',
      phone: '',
    }),
  }
</script>

<style>
.auth-form__container {
  height: 100%;
  width: 100%;
}

.auth-form__border {
  width: 100%;
  max-width: 600px;
  border-radius: 12px;
  padding: 52px 32px 0;
  position: relative;
  color: #95969D;
  background-clip: padding-box;

  &:before, &:after {
    content: '';
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
  }
  &:before {
    z-index: 1;
    margin: -1px;
    border-radius: inherit;
    background: linear-gradient(170deg, #86888F, black 50%);
  }
  &:after {
    z-index: 2;
    background: #020203;
    border-radius: inherit;
  }

  .auth-form__wrapper {
    position: relative;
    z-index: 5;
  }

  .auth-form__title.text-h4 {
    line-height: 2.125rem;
  }

  .input-group__label {
    padding: 1px 0;
    margin-bottom: 2px;
    color: #F5F5F6;
  }
  .input-group__input {
    border: 1px solid #272729;
    padding: 12px;
    border-radius: 6px;

    .v-input__slot {
      margin-bottom: 0;
      &:before, &:after {
        display: none;
      }
    }

    input {
      padding-top: 1px !important;
      padding-bottom: 1px !important;
    }
  }

  .btn-custom.btn-t2 {
    border: 1px solid #272729;
  }

  .btn-custom {
    text-transform: none;
  }
}
/* auth-form__border*/




.auth-form__footer {
  color: #95969D;

  a {
    color: #F5F5F6 !important;
    text-decoration: none;
  }
}

::placeholder {
  color: #A2A3A9 !important;
}
</style>
