<script setup>
import { useToast } from 'primevue/usetoast';
const toast = useToast();
</script>
<template>
    <Fluid>
        <div class="card flex flex-col gap-4 w-full">
            <div class="font-semibold text-xl mb-5">Create New User</div>
            <div class="flex flex-col md:flex-row gap-4">
                <div class="flex flex-wrap gap-2 w-full">
                    <label for="firstname">Firstname</label>
                    <InputText id="firstname" type="text" />
                </div>
                <div class="flex flex-wrap gap-2 w-full">
                    <label for="lastname">Lastname</label>
                    <InputText id="lastname" type="text" />
                </div>
            </div>
            <div class="flex flex-col md:flex-row gap-4">
                <div class="flex flex-wrap gap-2 w-full">
                    <label for="employeecode">Employee Code</label>
                    <InputText id="employeecode" type="text" />
                </div>
                <div class="flex flex-wrap gap-2 w-full">
                    <label for="officephone">Office Phone</label>
                    <InputText id="officephone" type="tel" />
                </div>

                <div class="flex flex-wrap gap-2 w-full">
                    <label for="jobtitle">Job Title</label>
                    <InputText id="jobtitle" type="text" />
                </div>
            </div>
            <div class="flex flex-col md:flex-row gap-4">
                <div class="flex flex-wrap gap-2 w-full">
                    <label for="factory">Factory</label>
                    <Select id="factory" v-model="dropdownItem" :options="dropdownItems" optionLabel="name" placeholder="Select One" class="w-full"></Select>
                </div>
                <div class="flex flex-wrap gap-2 w-full">
                    <label for="department">Department</label>
                    <Select id="department" v-model="dropdownItem" :options="dropdownItems" optionLabel="name" placeholder="Select One" class="w-full"></Select>
                </div>
            </div>
            <div class="flex flex-col md:flex-row gap-4">
                <div class="flex flex-wrap gap-2"><Button label="Create"></Button></div>
            </div>
        </div>
    </Fluid>
</template>
