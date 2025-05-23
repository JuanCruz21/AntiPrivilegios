<script>
  import { onMount } from 'svelte';
  import { FileDown,Twitter,Instagram,MonitorPlay,Users,Image,CloudDownload } from '@lucide/svelte';
  let mobileMenuOpen = $state(false);
  
  function toggleMobileMenu() {
    mobileMenuOpen = !mobileMenuOpen;
  }
  
  function closeMobileMenu() {
    mobileMenuOpen = false;
  }
</script>

<div class="min-h-screen bg-white">
  <!-- Header -->
  <header class="bg-white shadow-sm sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center py-3">
        <!-- Logo -->
        <div class="flex items-center space-x-3">
          <img 
          src="https://static.wixstatic.com/media/0f3c4e_4928004d3e4544659cda984d716d99d6~mv2.png/v1/crop/x_55,y_105,w_1370,h_240/fill/w_588,h_103,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/TWITER%20COLOR.png" 
          alt="Logo">
        </div>
        
        <!-- Desktop Social Icons -->
        <div class="hidden md:flex items-center space-x-2">
          <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
            <Twitter/>
          </a>
          <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
            <Twitter/>
          </a>
          <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M12.017 0C5.396 0 .029 5.367.029 11.987c0 5.079 3.158 9.417 7.618 11.174-.105-.949-.199-2.403.041-3.439.219-.937 1.406-5.957 1.406-5.957s-.359-.72-.359-1.781c0-1.663.967-2.911 2.168-2.911 1.024 0 1.518.769 1.518 1.688 0 1.029-.653 2.567-.992 3.992-.285 1.193.6 2.165 1.775 2.165 2.128 0 3.768-2.245 3.768-5.487 0-2.861-2.063-4.869-5.008-4.869-3.41 0-5.409 2.562-5.409 5.199 0 1.033.394 2.143.889 2.741.099.12.112.225.085.345-.09.375-.293 1.199-.334 1.363-.053.225-.172.271-.402.165-1.495-.69-2.433-2.878-2.433-4.646 0-3.776 2.748-7.252 7.92-7.252 4.158 0 7.392 2.967 7.392 6.923 0 4.135-2.607 7.462-6.233 7.462-1.214 0-2.357-.629-2.746-1.378l-.748 2.853c-.271 1.043-1.002 2.35-1.492 3.146C9.57 23.812 10.763 24.009 12.017 24.009c6.624 0 11.99-5.367 11.99-11.988C24.007 5.367 18.641.001 12.017.001z"/>
            </svg>
          </a>
          <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
            <Instagram/>
          </a>
        </div>
        
        <!-- Mobile menu a -->
        <a 
          on:click={toggleMobileMenu}
          class="md:hidden p-2 rounded-md text-gray-600 hover:text-teal-600 hover:bg-gray-100 transition-colors"
        >
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </a>
      </div>
      
      <!-- Mobile menu -->
      {#if mobileMenuOpen}
        <div class="md:hidden border-t border-gray-200 py-4">
          <div class="flex justify-center space-x-6">
            <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M22.46 6c-.77.35-1.6.58-2.46.69.88-.53 1.56-1.37 1.88-2.38-.83.5-1.75.85-2.72 1.05C18.37 4.5 17.26 4 16 4c-2.35 0-4.27 1.92-4.27 4.29 0 .34.04.67.11.98C8.28 9.09 5.11 7.38 3 4.79c-.37.63-.58 1.37-.58 2.15 0 1.49.75 2.81 1.91 3.56-.71 0-1.37-.2-1.95-.5v.03c0 2.08 1.48 3.82 3.44 4.21a4.22 4.22 0 0 1-1.93.07 4.28 4.28 0 0 0 4 2.98 8.521 8.521 0 0 1-5.33 1.84c-.34 0-.68-.02-1.02-.06C3.44 20.29 5.7 21 8.12 21 16 21 20.33 14.46 20.33 8.79c0-.19 0-.37-.01-.56.84-.6 1.56-1.36 2.14-2.23z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12.017 0C5.396 0 .029 5.367.029 11.987c0 5.079 3.158 9.417 7.618 11.174-.105-.949-.199-2.403.041-3.439.219-.937 1.406-5.957 1.406-5.957s-.359-.72-.359-1.781c0-1.663.967-2.911 2.168-2.911 1.024 0 1.518.769 1.518 1.688 0 1.029-.653 2.567-.992 3.992-.285 1.193.6 2.165 1.775 2.165 2.128 0 3.768-2.245 3.768-5.487 0-2.861-2.063-4.869-5.008-4.869-3.41 0-5.409 2.562-5.409 5.199 0 1.033.394 2.143.889 2.741.099.12.112.225.085.345-.09.375-.293 1.199-.334 1.363-.053.225-.172.271-.402.165-1.495-.69-2.433-2.878-2.433-4.646 0-3.776 2.748-7.252 7.92-7.252 4.158 0 7.392 2.967 7.392 6.923 0 4.135-2.607 7.462-6.233 7.462-1.214 0-2.357-.629-2.746-1.378l-.748 2.853c-.271 1.043-1.002 2.35-1.492 3.146C9.57 23.812 10.763 24.009 12.017 24.009c6.624 0 11.99-5.367 11.99-11.988C24.007 5.367 18.641.001 12.017.001z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-600 hover:text-teal-600 transition-colors">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
              </svg>
            </a>
          </div>
        </div>
      {/if}
    </div>
  </header>

  <!-- Hero Section -->
  <section class="relative bg-gradient-to-br from-teal-600 via-teal-700 to-blue-800 overflow-hidden">
    <!-- Background overlay -->
    <div class="absolute inset-0 bg-black bg-opacity-40"></div>
    
    <!-- Hero image -->
    <div class="absolute inset-0">
      <img 
        src="https://static.wixstatic.com/media/0f3c4e_9cf0fd61e016467b9db19b39ea574939~mv2.jpg/v1/fill/w_1845,h_323,al_c,q_85,usm_0.66_1.00_0.01,enc_avif,quality_auto/0f3c4e_9cf0fd61e016467b9db19b39ea574939~mv2.jpg?height=600&width=1200" 
        alt="Grupo de personas sonriendo con carteles del referendo antiprivilegios"
        class="w-full h-full object-cover blur-sm"
      />
    </div>
    
    <!-- Content -->
    <div class="relative max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16 sm:py-24 lg:py-32">
      <div class="text-center">
        <h1 class="text-3xl sm:text-4xl lg:text-6xl font-bold text-white mb-6 leading-tight">
          Referendo Antiprivilegios<br>
          <span class="text-yellow-400">de Congresistas</span>
        </h1>
        <p class="text-lg sm:text-xl text-gray-200 mb-12 max-w-3xl mx-auto">
          Únete al movimiento ciudadano para eliminar los privilegios excesivos de los congresistas y construir una democracia más justa y transparente.
        </p>
        
        <!-- Action as -->
        <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 sm:gap-6 max-w-4xl mx-auto">
          <!-- Formulario -->
          <div class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1">
            <div class="flex flex-col items-center text-center">
              <div class="bg-teal-100 p-3 rounded-full mb-4">
                <FileDown/>
              </div>
              <h3 class="text-xl font-bold text-gray-900 mb-2">FORMULARIO</h3>
              <p class="text-gray-600 mb-4 text-sm">Imprimir formulario</p>
              <a href="#" 
                class="bg-teal-600 text-white px-6 py-2 rounded-lg hover:bg-teal-700 transition-colors font-medium"
              >
                Descargar
              </a>
            </div>
          </div>
          
          <!-- Tutorial -->
          <div class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1">
            <div class="flex flex-col items-center text-center">
              <div class="bg-red-100 p-3 rounded-full mb-4">
                <MonitorPlay/>
              </div>
              <h3 class="text-xl font-bold text-gray-900 mb-2">TUTORIAL</h3>
              <p class="text-gray-600 mb-4 text-sm">Cómo diligenciar el formulario</p>
              <a href="#" class="bg-red-600 text-white px-6 py-2 rounded-lg hover:bg-red-700 transition-colors font-medium">
                Ver Video
              </a>
            </div>
          </div>
          
          <!-- Voluntarios -->
          <div class="bg-white rounded-xl shadow-lg p-6 hover:shadow-xl transition-all duration-300 transform hover:-translate-y-1">
            <div class="flex flex-col items-center text-center">
              <div class="bg-yellow-100 p-3 rounded-full mb-4">
                <Users/>
              </div>
              <h3 class="text-xl font-bold text-gray-900 mb-2">VOLUNTARIOS</h3>
              <p class="text-gray-600 mb-4 text-sm">Inscripción de voluntarios</p>
              <a href="#" class="bg-yellow-600 text-white px-6 py-2 rounded-lg hover:bg-yellow-700 transition-colors font-medium">
                Inscribirse
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Information Section -->
  <section class="bg-gray-50 py-16 sm:py-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16">
        <!-- Left Column -->
        <div>
          <h2 class="text-3xl sm:text-4xl font-bold text-gray-900 mb-8">
            Dónde Enviar<br>
            <span class="text-teal-600">Formularios Firmados</span>
          </h2>
          
          <div class="space-y-6">
            <div class="bg-white rounded-lg p-6 shadow-md">
              <h3 class="text-xl font-semibold text-gray-900 mb-3">Sede Principal</h3>
              <div class="flex items-start space-x-3">
                <svg class="w-6 h-6 text-teal-600 mt-1 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path>
                </svg>
                <div>
                  <p class="text-gray-700 font-medium">CARRERA 1 ESTE # 72A - 15</p>
                  <p class="text-gray-600">(BOGOTÁ - COLOMBIA)</p>
                </div>
              </div>
            </div>
            
            <div class="bg-white rounded-lg p-6 shadow-md">
              <h3 class="text-xl font-semibold text-gray-900 mb-3">Otras Ciudades</h3>
              <a href="#" class="text-teal-600 hover:text-teal-700 font-medium underline transition-colors">
                (CLIC AQUÍ)
              </a>
            </div>
          </div>
        </div>
        
        <!-- Right Column -->
        <div class="space-y-8">
          <div class="bg-white rounded-lg p-8 shadow-md">
            <h3 class="text-2xl font-bold text-gray-900 mb-6">Documentos Importantes</h3>
            
            <div class="space-y-4">
              <a href="#" class="w-full bg-teal-600 text-white py-4 px-6 rounded-lg hover:bg-teal-700 transition-colors flex items-center justify-center space-x-3 font-medium">
                <CloudDownload/>
                <span>DESCARGAR TEXTO DEL REFERENDO</span>
              </a>
              
              <a href="#" class="w-full bg-gray-800 text-white py-4 px-6 rounded-lg hover:bg-gray-900 transition-colors flex items-center justify-center space-x-3 font-medium">
                <Image/>
                <span>DESCARGAR LOGO</span>
              </a>
            </div>
          </div>
          
          <!-- Stats or additional info -->
          <div class="bg-gradient-to-r from-teal-600 to-blue-600 rounded-lg p-8 text-white">
            <h3 class="text-2xl font-bold mb-4">¿Por qué es importante?</h3>
            <ul class="space-y-3 text-teal-100">
              <li class="flex items-start space-x-2">
                <svg class="w-5 h-5 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                </svg>
                <span>Reducir gastos innecesarios del Estado</span>
              </li>
              <li class="flex items-start space-x-2">
                <svg class="w-5 h-5 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                </svg>
                <span>Promover la transparencia política</span>
              </li>
              <li class="flex items-start space-x-2">
                <svg class="w-5 h-5 mt-0.5 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                </svg>
                <span>Fortalecer la democracia participativa</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-gray-900 text-white py-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <h3 class="text-2xl font-bold mb-4">REFERENDO ANTIPRIVILEGIOS DE CONGRESISTAS</h3>
        <div class="space-y-2 mb-8">
          <p class="text-gray-300">
            <span class="font-medium">Contacto:</span> 
            <a href="mailto:antiprivilegios@gmail.com" class="text-teal-400 hover:text-teal-300 transition-colors">
              antiprivilegios@gmail.com
            </a>
          </p>
        </div>
        
        <!-- Social links -->
        <div class="flex justify-center space-x-6 mb-8">
          <a href="#" class="text-gray-400 hover:text-white transition-colors">
            <Twitter/>
          </a>
          <a href="#" class="text-gray-400 hover:text-white transition-colors">
            <Twitter/>
          </a>
          <a href="#" class="text-gray-400 hover:text-white transition-colors">
            <Instagram/>
          </a>
        </div>
        
        <div class="border-t border-gray-800 pt-8">
          <p class="text-gray-400 text-sm">
            Copyright © 2025 · All Rights Reserved
          </p>
        </div>
      </div>
    </div>
  </footer>
</div>
