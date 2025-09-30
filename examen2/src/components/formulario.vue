<template>
  <div class="form-wrapper">
    <div class="container">
      <div class="card shadow-lg rounded-4 border-0">
        <div class="card-header bg-gradient-primary text-white text-center rounded-top-4">
          <h3><i class="bi bi-person-circle me-2"></i>Formulario de Registro</h3>
        </div>
        <div class="card-body bg-light">
          <form @submit.prevent="enviarFormulario">
            <div class="mb-4">
              <label for="nombre" class="form-label fw-bold">Nombre</label>
              <input type="text" id="nombre" v-model="form.nombre" class="form-control form-control-lg" required placeholder="Ingresa tu nombre">
            </div>
            <div class="mb-4">
              <label for="email" class="form-label fw-bold">Correo Electrónico</label>
              <input type="email" id="email" v-model="form.email" class="form-control form-control-lg" required placeholder="ejemplo@correo.com">
            </div>
            <div class="mb-4">
              <label for="password" class="form-label fw-bold">Contraseña</label>
              <input type="password" id="password" v-model="form.password" class="form-control form-control-lg" required placeholder="********">
            </div>
            <div class="d-grid gap-2">
              <button type="submit" class="btn btn-success btn-lg shadow-sm">
                <i class="bi bi-send-fill me-2"></i>Enviar
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        nombre: '',
        email: '',
        password: ''
      }
    }
  },
  methods: {
    enviarFormulario() {
      window.location.href = "https://www.youtube.com/watch?v=LPBF0EjZP4k";
    }
  }
}
</script>

<style scoped>
.form-wrapper {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(120deg, #e3eafc 60%, #f8fafc 100%);
}
.container {
  max-width: 700px;
  width: 100%;
}
.card {
  background: linear-gradient(135deg, #f8fafc 60%, #e3eafc 100%);
}
.card-header {
  background: linear-gradient(90deg, #007bff 60%, #00c6ff 100%);
  box-shadow: 0 2px 8px rgba(0,0,0,0.08);
}
.card-body {
  padding: 2.5rem;
}
.form-label {
  color: #007bff;
}
input:focus {
  border-color: #00c6ff;
  box-shadow: 0 0 0 0.2rem rgba(0,198,255,.25);
}
.btn-success {
  background: linear-gradient(90deg, #28a745 60%, #5afc8b 100%);
  border: none;
}
.btn-success:hover {
  background: linear-gradient(90deg, #218838 60%, #43e97b 100%);
}
</style>