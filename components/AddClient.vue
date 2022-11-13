<template>
    <div class="ma-3">
        <v-card-title>
            Add New Client
        </v-card-title>
            <v-text-field v-model="data.Full_nam"  @change="emitData" label="Full name" >Full Name</v-text-field>
            <v-text-field v-model="data.Address"  @change="emitData" label="Address" >Address</v-text-field>
            <v-text-field v-model="data.Wilaya"  @change="emitData" label="Wilaya" >Wilaya</v-text-field>
            <v-text-field v-model="data.Phone_numbe"  @change="emitData" label="Phone number" >Phone number</v-text-field>
            <v-text-field v-model="data.Items"  @change="emitData" label="Items" >Items</v-text-field>
            <v-text-field v-model="data.Shiping"  @change="emitData" label="Shiping" >Shiping</v-text-field>
            <v-text-field v-model="data.Total"  @change="emitData" label="Total" >Total</v-text-field>
    </div>
</template>
<script>
export default {
    data() {
        return {
            overlay: false,
            zIndex: 0,
            data: {
                Full_nam: '',
                Address: '',
                Wilaya: '',
                Phone_numbe: '',
                Items: '',
                Shiping: '',
                Total: '',
            }
        }
    },
    methods: {
        emitData() {
            this.$emit('onadd', this.data);
        }
    },
}
</script>
