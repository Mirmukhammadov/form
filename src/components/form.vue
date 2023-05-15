<template>
  <div class="w-[900px] mx-auto">
    <h1 class="text-[#131313] text-[28px] mb-4">Local application</h1>
    <div class="bg-[#f7f7f7] p-6 flex flex-wrap">
      <div class="flex flex-col mb-6 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >First name <span class="text-[red]">*</span></label
        >
        <Dinput
          placeholder="Your first name"
          v-model="state.firstNameValue"
          label="Input 1"
          type="text"
          :allstyle="allstyle"
          :class="{ 'border-[red]': firstNameError }"
        />
        <span
          v-if="firstNameError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 2 -->

      <div class="flex flex-col mb-6 ml-5 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Last name <span class="text-[red]">*</span></label
        >
        <Dinput
          placeholder="Your last name"
          v-model="state.lastNameValue"
          label="Input 1"
          type="text"
          :allstyle="allstyle"
          :class="{ 'border-[red]': lastNameError }"
        />
        <span
          v-if="lastNameError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 3 -->
      <div class="flex flex-col mb-6 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Father’s name <span class="text-[red]">*</span></label
        >
        <Dinput
          placeholder="Your father’s name"
          v-model="state.fathersName"
          label="Input 1"
          type="text"
          :allstyle="allstyle"
          :class="{ 'border-[red]': fathersError }"
        />
        <span
          v-if="fathersError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 4 -->

      <div class="flex flex-col ml-5 mb-6 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Gender <span class="text-[red]">*</span></label
        >
        <select
          name=""
          id=""
          class="bg-[#ececef] w-[400px] p-[15px] text-[#ABABAF] font-medium text-[16px] rounded-lg outline-none"
          v-model="state.gender"
          :allstyle="allstyle"
          :class="{ 'border-[red]': genderError }"
        >
          <option
            value=""
            style="background-image: url(../assets/images/Vector.svg)"
            disabled
          >
            Select your gender
          </option>
          <option value="1">1</option>
          <option value="2">2</option>
        </select>
        <span
          v-if="genderError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 5 -->

      <div class="flex flex-col mb-6 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Country/Place of birth <span class="text-[red]">*</span></label
        >
        <Dinput
          placeholder="Your Country/Place of birth"
          v-model="state.placeOfBirth"
          label="Input 1"
          type="text"
          :allstyle="allstyle"
          :class="{ 'border-[red]': placeOfBirthError }"
        />
        <span
          v-if="placeOfBirthError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 6 -->

      <div class="flex flex-col mb-6 ml-5 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >City/Province <span class="text-[red]">*</span></label
        >
        <Dinput
          placeholder="Your City/Province"
          v-model="state.city"
          label="Input 1"
          type="text"
          :allstyle="allstyle"
          :class="{ 'border-[red]': cityError }"
        />
        <span
          v-if="cityError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 7 -->

      <div class="flex flex-col relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Nationality <span class="text-[red]">*</span></label
        >
        <select
          name=""
          id=""
          v-model="state.nationality"
          :allstyle="allstyle"
          class="bg-[#ececef] w-[400px] p-[15px] text-[#ABABAF] font-medium text-[16px] rounded-lg outline-none"
          :class="{ 'border-[red]': nationalityError }"
        >
          <option
            value=""
            style="background-image: url(../assets/images/Vector.svg)"
            disabled
          >
            Select your nationality
          </option>
          <option value="3">1</option>
          <option value="4">2</option>
        </select>
        <span
          v-if="nationalityError"
          class="absolute bottom-[0px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 8 -->
      <div class="flex flex-col mb-6 ml-5 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Passport/ID card serial number<span class="text-[red]"
            >*</span
          ></label
        >
        <Dinput
          placeholder="Your Passport/ID card serial number "
          v-model="state.cardId"
          label="Input 1"
          type="password"
          :allstyle="allstyle"
          :class="{ 'border-[red]': cardIdError }"
        />
        <span
          v-if="cardIdError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 9 -->
      <div class="flex flex-col mb-6 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Phone number <span class="text-[red]">*</span></label
        >
        <Dinput
          defaultValue="+998"
          v-model="state.phoneNumber"
          label="Input 1"
          type="text"
          :allstyle="allstyle"
          :class="{ 'border-[red]': phoneNumberError }"
        />
        <span
          v-if="phoneNumberError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 10 -->
      <div class="flex flex-col mb-6 ml-5 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Email <span class="text-[red]">*</span></label
        >
        <Dinput
          placeholder="example@tmci.uz"
          v-model="state.email"
          label="Input 1"
          type="email"
          :allstyle="allstyle"
          :class="{ 'border-[red]': emailError }"
        />
        <span
          v-if="emailError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <!-- 11 -->
      <div class="flex flex-col mb-6 relative">
        <label
          for=""
          class="text-[#506277] font-medium text-[16px] leading-[130%] pb-2"
          >Emergency contact <span class="text-[red]">*</span></label
        >
        <Dinput
          defaultValue="+998"
          v-model="state.emergencyContact"
          label="Input 1"
          type="text"
          :allstyle="allstyle"
          :class="{ 'border-[red]': emergencyContactError }"
        />
        <span
          v-if="emergencyContactError"
          class="absolute bottom-[-20px] text-[15px] text-[red]"
          >fill the field correct</span
        >
      </div>

      <div class="flex w-[900px] justify-end">
        <button class="bg-[#ABABAF] rounded-2xl text-[#FFF] px-[90px] py-5">
          back
        </button>
        <button
          class="bg-[#971837] rounded-2xl text-[#FFF] px-[90px] py-5 ml-4"
          @click="validateForm"
        >
          Continue
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Dinput from "./input.vue";

import { useVuelidate } from "@vuelidate/core";
import { minLength, required, email } from "@vuelidate/validators";

const types = ref({
  text: "text",
  password: "password",
  number: "number",
});

const state = ref({
  firstNameValue: "",
  lastNameValue: "",
  fathersName: "",
  gender: "",
  placeOfBirth: "",
  city: "",
  nationality: "",
  cardId: "",
  phoneNumber: "+998",
  email: "",
  emergencyContact: "+998",
});

const rules = {
  firstNameValue: { required },
  lastNameValue: { required },
  fathersName: { required },
  gender: { required },
  placeOfBirth: { required },
  nationality: { required },
  city: { required },
  cardId: { required },
  phoneNumber: { required, minLength: minLength(13) },
  email: { required, email },
  emergencyContact: { required, minLength: minLength(13) },
};

const v$ = useVuelidate(rules, state);
const allstyle = ref(false);

const firstNameError = ref(false);
const lastNameError = ref(false);
const fathersError = ref(false);
const genderError = ref(false);
const placeOfBirthError = ref(false);
const cityError = ref(false);
const nationalityError = ref(false);
const cardIdError = ref(false);
const phoneNumberError = ref(false);
const emailError = ref(false);
const emergencyContactError = ref(false);

function validateForm() {
  v$.value.$validate();

  if (v$.value.$error) {
    allstyle.value = true;
  } else {
    allstyle.value = false;
  }

  firstNameError.value = v$.value.firstNameValue.$error;
  lastNameError.value = v$.value.lastNameValue.$error;
  fathersError.value = v$.value.fathersName.$error;
  genderError.value = v$.value.gender.$error;
  placeOfBirthError.value = v$.value.placeOfBirth.$error;
  cityError.value = v$.value.city.$error;
  nationalityError.value = v$.value.nationality.$error;
  cardIdError.value = v$.value.cardId.$error;
  phoneNumberError.value = v$.value.phoneNumber.$error;
  emailError.value = v$.value.email.$error;
  emergencyContactError.value = v$.value.emergencyContact.$error;

  console.log(
    firstNameError.value,
    lastNameError.value,
    fathersError.value,
    genderError.value,
    placeOfBirthError.value,
    cityError.value,
    nationalityError.value,
    cardIdError.value,
    phoneNumberError.value,
    emailError.value,
    emergencyContactError.value
  );
}
</script>
