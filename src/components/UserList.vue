<template>
    <div>
        <button @click="addUser">Add User</button>
        <ul>
            <li v-for="(user, index) in userList" :key="index">
                <span>{{ user.name }}</span>
                <span>{{ user.city }}</span>
                <span>{{ user.gender }}</span>
                <!-- Add other desired fields here -->
                <button @click="deleteUser(index)">Delete</button>
                <button @click="updateUser(user)">Update</button>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data() {
        return {
            userList: []
        };
    },
    methods: {
        async addUser() {
            const response = await fetch('https://randomuser.me/api/?results=5');
        },
        deleteUser(index) {
            // Remove the user at the specified index from the userList array
            this.userList.splice(index, 1);
        },
        updateUser(user) {
            // Update the properties of the user object
            // You can show a form or input fields to update the desired fields
        }
    }
};
</script>
