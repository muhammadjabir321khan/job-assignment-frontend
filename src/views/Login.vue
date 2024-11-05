<script setup>
import useAuth from '@/composable/login';
const { loginWithGoogle } = useAuth();

const googleLogin = () => {
  loginWithGoogle();
};
</script>

<template>
  <div class="container-fluid h-100 " >
    <div class="row justify-content-center align-items-center h-100">
      <div class="col-md-5 col-lg-4">
        <div class="card shadow">
          <div class="card-body">
            <h5 class="card-title text-center mb-4">Log in to Your Account</h5>
            <p class="text-center mb-4">Enhance Your Website's Performance with Google Lighthouse API.</p>
            <button @click="googleLogin" class="btn btn-outline-success w-100">
              <img src="/src/assets/logo/download.svg" alt="Google logo" class="google-logo" />
              Log in with Google
            </button>
            <hr class="my-4" />
            <p class="text-center">Don't have an account? <a href="#" class="text-success">Sign up</a></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
html, body {
  height: 100%;
  margin: 0; 
  font-family: Arial, sans-serif; 
}

.row {
  min-height: 100vh; 
}

.card {
  margin: 30px; 
  border-radius: 8px; 
}

.card-title {
  font-size: 1.5rem; 
  font-weight: bold; 
}

.card-text {
  font-size: 1rem; 
  color: #555; 
}

.btn {
  font-weight: 600; 
}

.google-logo {
  width: 20px;
  margin-right: 5px; 
}

.text-success {
  color: #28a745; 
}

.btn-outline-success {
  border-color: #28a745; 
  color: #28a745;
}

.btn-outline-success:hover {
  background-color: #28a745; 
  color: white; 
}
</style>
