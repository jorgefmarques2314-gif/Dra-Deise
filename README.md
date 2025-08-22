<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dra. Deise Luci | Psicóloga e Especialista em Desenvolvimento Humano</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Source+Sans+Pro:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'gold': '#D4AF37',
                        'pure-black': '#000000',
                        'pure-white': '#FFFFFF'
                    },
                    fontFamily: {
                        'playfair': ['Playfair Display', 'serif'],
                        'sans': ['Source Sans Pro', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <style>
        /* Efeitos e animações personalizados */
        .rotating-text { min-height: 60px; }
        .floating-element {
            box-shadow: 0 15px 35px rgba(212, 175, 55, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: float 6s ease-in-out infinite;
        }
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        .section-divider {
            position: absolute;
            bottom: -1px;
            left: 0;
            width: 100%;
            overflow: hidden;
            line-height: 0;
            transform: rotate(180deg);
        }
        .section-divider svg {
            position: relative;
            display: block;
            width: calc(100% + 1.3px);
            height: 70px;
        }
        .testimonial-card,
        .video-card {
            transform: scale(0.95);
            transition: all 0.3s ease;
            opacity: 0.75;
        }
        .testimonial-card.active,
        .video-card.active {
            transform: scale(1);
            opacity: 1;
        }
    </style>
</head>
<body class="bg-pure-black font-sans text-pure-white">
    <!-- Atalho de WhatsApp flutuante -->
    <a href="https://wa.me/5511958030707" target="_blank" class="fixed right-6 bottom-6 z-50 bg-[#25D366] rounded-full p-3 shadow-lg hover:scale-105 transition-transform">
        <i class="fab fa-whatsapp text-3xl text-pure-white"></i>
    </a>

    <!-- Menu de Navegação Fixo -->
    <nav id="navigation" class="fixed top-0 w-full z-50 bg-pure-black bg-opacity-90 backdrop-blur-sm py-3 transition-all">
        <div class="container mx-auto px-6 flex flex-wrap justify-between items-center">
            <a href="#inicio" class="flex items-center">
                <img src="https://i.postimg.cc/qvn7dQmh/IMG-9989.jpg" alt="Logo Dra. Deise Luci" class="h-12 w-12 rounded-full object-cover">
                <span class="ml-3 font-playfair text-gold text-xl">Dra. Deise Luci</span>
            </a>
            
            <button id="menu-toggle" class="block md:hidden text-gold">
                <i class="fas fa-bars text-2xl"></i>
            </button>
            
            <div id="menu-items" class="hidden md:flex flex-col md:flex-row justify-center text-center md:text-left w-full md:w-auto mt-4 md:mt-0">
                <a href="#sobre" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Sobre</a>
                <a href="#areas" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Áreas de Atuação</a>
                <a href="#programas" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Programas</a>
                <a href="#saude" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Saúde Mental</a>
                <a href="#certificacoes" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Certificações</a>
                <a href="#depoimentos" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Depoimentos</a>
                <a href="#videos" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Vídeos</a>
                <a href="#contato" class="py-2 px-4 text-gold hover:text-pure-white transition-colors">Contato</a>
            </div>
        </div>
    </nav>

    <!-- Seção Início/Hero -->
    <section id="inicio" class="min-h-screen relative flex items-center bg-pure-black">
        <div class="section-divider">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M1200 120L0 16.48 0 0 1200 0 1200 120z" class="shape-fill" fill="#D4AF37"></path>
            </svg>
        </div>
        
        <div class="container mx-auto px-6 py-32 md:py-0 flex flex-col-reverse lg:flex-row items-center justify-between">
            <div class="lg:w-1/2 text-center lg:text-left mt-12 lg:mt-0">
                <h1 class="mt-10 font-playfair text-4xl md:text-5xl lg:text-6xl leading-tight text-pure-white">
                    Dra. Deise Luci
                    <div class="rotating-text block h-16 text-gold text-3xl mt-4">
                        <span id="rotating-phrase" class="fade-in">Agente Transformadora de Vidas</span>
                    </div>
                </h1>
                <p class="mt-6 text-xl text-pure-white opacity-90">
                    Psicóloga, Palestrante e Especialista em Desenvolvimento Humano
                </p>
                <div class="mt-8 flex flex-wrap gap-4 justify-center lg:justify-start">
                    <a href="https://wa.me/5511958030707" target="_blank" class="bg-gold text-pure-black py-3 px-8 rounded-full font-bold transition-all hover:bg-pure-white flex items-center gap-2">
                        <i class="fab fa-whatsapp"></i> WhatsApp
                    </a>
                    <button class="bg-transparent border-2 border-gold text-gold py-3 px-8 rounded-full font-bold transition-all hover:bg-gold hover:text-pure-black">
                        <i class="fas fa-calendar-check mr-2"></i>Agendar Consultoria
                    </button>
                </div>
            </div>
            
            <div class="relative lg:w-1/2 flex justify-center">
                <div class="relative floating-element">
                    <img src="https://i.postimg.cc/QCSg8h0t/Whats-App-Image-2025-08-21-at-16-19-23-3.jpg" alt="Dra. Deise Luci" class="rounded-3xl w-96 h-96 object-cover">
                    <div class="absolute -inset-4 rounded-3xl border-4 border-gold z-[-1]"></div>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Sobre -->
    <section id="sobre" class="relative py-24 bg-pure-white">
        <div class="section-divider">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M1200 120L0 16.48 0 0 1200 0 1200 120z" class="shape-fill" fill="#000000"></path>
            </svg>
        </div>
        
        <div class="container mx-auto px-6 flex flex-col lg:flex-row items-center">
            <div class="lg:w-1/3 relative flex justify-center mb-12 lg:mb-0">
                <div class="floating-element">
                    <img src="https://i.postimg.cc/Y2XmCnth/Whats-App-Image-2025-08-20-at-10-27-01.jpg" alt="Dra. Deise Luci" class="rounded-3xl w-96 h-96 object-cover">
                    <div class="absolute -inset-4 rounded-3xl border-4 border-gold z-[-1]"></div>
                </div>
            </div>
            
            <div class="lg:w-2/3 lg:pl-16">
                <h2 class="font-playfair text-4xl md:text-5xl mb-8 text-pure-black">Sobre Dra. Deise Luci</h2>
                <p class="text-lg text-gray-800 leading-relaxed mb-6">
                    Psicóloga, Pós-graduada em Psicologia Positiva e Especialista em Desenvolvimento Humano. Com mais de 5.000 atendimentos realizados e mais de 50 mentorados acompanhados, ela é referência em saúde mental, liderança e transformação de pessoas e empresas.
                </p>
                <p class="text-lg text-gray-800 leading-relaxed mb-6">
                    Atua como palestrante em eventos nacionais e internacionais, consultora empresarial, mentora de líderes e CEO de programas como o <span class="font-semibold text-gold">Floreser Desenvolvimento de Pessoas</span>, projeto de impacto voltado para o crescimento pessoal e profissional.
                </p>
                <p class="text-lg text-gray-800 leading-relaxed">
                    Sua trajetória começou cedo: aos 11 anos já empreendia, e após mais de 15 anos no setor da beleza, encontrou na psicologia sua verdadeira missão. Desde 2013, acolheu e transformou a vida de milhares de mulheres, lideranças e organizações, sempre com ética, sensibilidade e foco em resultados. Sua missão é clara: fazer pessoas florescerem, despertarem seu verdadeiro potencial e conquistarem clareza, confiança e propósito de vida.
                </p>
            </div>
        </div>
    </section>

    <!-- Seção Áreas de Atuação -->
    <section id="areas" class="relative py-24 bg-gold">
        <div class="section-divider">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M1200 120L0 16.48 0 0 1200 0 1200 120z" class="shape-fill" fill="#FFFFFF"></path>
            </svg>
        </div>
        
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-playfair text-4xl md:text-5xl mb-8 text-pure-black">Áreas de Atuação</h2>
                <p class="text-xl text-pure-black max-w-3xl mx-auto">
                    Transformação individual e empresarial através de metodologias inovadoras e comprovadas
                </p>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16">
                <!-- Consultoria Individual -->
                <div class="bg-pure-black p-8 rounded-2xl hover:shadow-xl transition-shadow">
                    <i class="fas fa-user text-4xl text-gold mb-4"></i>
                    <h3 class="font-playfair text-2xl mb-4 text-pure-white">Consultoria Individual</h3>
                    <p class="text-pure-white">
                        Autoconhecimento, clareza de propósito, alta performance e quebra de crenças limitantes.
                    </p>
                </div>
                
                <!-- Consultoria Empresarial -->
                <div class="bg-pure-black p-8 rounded-2xl hover:shadow-xl transition-shadow">
                    <i class="fas fa-building text-4xl text-gold mb-4"></i>
                    <h3 class="font-playfair text-2xl mb-4 text-pure-white">Consultoria Empresarial</h3>
                    <p class="text-pure-white">
                        Avaliação de competências, treinamentos, gestão de equipes e aumento de performance.
                    </p>
                </div>
                
                <!-- Mentoria para Líderes -->
                <div class="bg-pure-black p-8 rounded-2xl hover:shadow-xl transition-shadow">
                    <i class="fas fa-chalkboard-teacher text-4xl text-gold mb-4"></i>
                    <h3 class="font-playfair text-2xl mb-4 text-pure-white">Mentoria para Líderes</h3>
                    <p class="text-pure-white">
                        Comunicação assertiva, gestão de pessoas, resolução de conflitos e liderança humanizada.
                    </p>
                </div>
                
                <!-- Programas Exclusivos -->
                <div class="bg-pure-black p-8 rounded-2xl hover:shadow-xl transition-shadow">
                    <i class="fas fa-star text-4xl text-gold mb-4"></i>
                    <h3 class="font-playfair text-2xl mb-4 text-pure-white">Programas Exclusivos</h3>
                    <p class="text-pure-white">
                        Processos de desenvolvimento humano para todas as necessidades com resultados comprovados.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Programas -->
    <section id="programas" class="py-24 bg-pure-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-playfair text-4xl md:text-5xl mb-6 text-pure-black">Programas Exclusivos</h2>
            </div>
            
            <div class="grid md:grid-cols-2 gap-12">
                <!-- Floreser Desenvolvimento de Pessoas -->
                <div class="bg-gold p-8 rounded-2xl hover:shadow-xl transition-all">
                    <div class="flex items-center mb-4">
                        <div class="bg-pure-black text-gold w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-brain"></i>
                        </div>
                        <h3 class="font-playfair text-2xl text-pure-black">Floreser Desenvolvimento de Pessoas</h3>
                    </div>
                    <p class="text-pure-black">
                        Consultoria e treinamentos em desenvolvimento humano para impulsionar a transformação pessoal e profissional.
                    </p>
                </div>
                
                <!-- Flore-Ser Mulher -->
                <div class="bg-gold p-8 rounded-2xl hover:shadow-xl transition-all">
                    <div class="flex items-center mb-4">
                        <div class="bg-pure-black text-gold w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-female"></i>
                        </div>
                        <h3 class="font-playfair text-2xl text-pure-black">Flore-Ser Mulher</h3>
                    </div>
                    <p class="text-pure-black">
                        Programa dedicado ao desenvolvimento pessoal e profissional feminino, fortalecendo identidade e poder.
                    </p>
                </div>
                
                <!-- Flore-Ser Homem -->
                <div class="bg-gold p-8 rounded-2xl hover:shadow-xl transition-all">
                    <div class="flex items-center mb-4">
                        <div class="bg-pure-black text-gold w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-male"></i>
                        </div>
                        <h3 class="font-playfair text-2xl text-pure-black">Flore-Ser Homem</h3>
                    </div>
                    <p class="text-pure-black">
                        Estruturação de fortalecimento de posicionamento, disciplina e propósito masculino.
                    </p>
                </div>
                
                <!-- Tire Seu Sonho do Papel -->
                <div class="bg-gold p-8 rounded-2xl hover:shadow-xl transition-all">
                    <div class="flex items-center mb-4">
                        <div class="bg-pure-black text-gold w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-rocket"></i>
                        </div>
                        <h3 class="font-playfair text-2xl text-pure-black">Tire Seu Sonho do Papel</h3>
                    </div>
                    <p class="text-pure-black">
                        Mentoria em organização, produtividade e transição de carreira para concretização de projetos de vida.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Saúde Mental -->
    <section id="saude" class="relative py-24 bg-pure-black">
        <div class="section-divider">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M1200 120L0 16.48 0 0 1200 0 1200 120z" class="shape-fill" fill="#D4AF37"></path>
            </svg>
        </div>
        
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-playfair text-4xl md:text-5xl mb-6 text-gold">Saúde Mental</h2>
                <p class="text-xl text-pure-white max-w-3xl mx-auto">
                    Cuidados especializados para indivíduos e corporações, promovendo qualidade de vida e bem-estar psicológico.
                </p>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-gold bg-opacity-10 backdrop-blur-sm border border-gold p-8 rounded-2xl text-pure-white">
                    <h3 class="font-playfair text-2xl mb-4 text-gold">Promoção de Saúde Mental</h3>
                    <p>Escuta ativa, rodas de conversa e programas de acolhimento desenvolvidos para criar ambientes saudáveis.</p>
                </div>
                
                <div class="bg-gold bg-opacity-10 backdrop-blur-sm border border-gold p-8 rounded-2xl text-pure-white">
                    <h3 class="font-playfair text-2xl mb-4 text-gold">CNV - Comunicação Não Violenta</h3>
                    <p>Aplicação da técnica em ambientes corporativos e pessoais para melhorar relacionamentos e interações.</p>
                </div>
                
                <div class="bg-gold bg-opacity-10 backdrop-blur-sm border border-gold p-8 rounded-2xl text-pure-white">
                    <h3 class="font-playfair text-2xl mb-4 text-gold">Projetos de Enfrentamento ao Burnout</h3>
                    <p>Diagnósticos precisos, estratégias efetivas e protocolos de cuidado para combater a síndrome de burnout.</p>
                </div>
                
                <div class="bg-gold bg-opacity-10 backdrop-blur-sm border border-gold p-8 rounded-2xl text-pure-white">
                    <h3 class="font-playfair text-2xl mb-4 text-gold">Programa "Cuca Fresca"</h3>
                    <p>Plantão psicológico corporativo com atendimentos individuais e em grupo para saúde mental no trabalho.</p>
                </div>
                
                <div class="bg-gold bg-opacity-10 backdrop-blur-sm border border-gold p-8 rounded-2xl text-pure-white">
                    <h3 class="font-playfair text-2xl mb-4 text-gold">Psicoterapia</h3>
                    <p>Atendimentos psicológicos on-line e presenciais, personalizados para cada necessidade específica.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Certificações -->
    <section id="certificacoes" class="py-24 bg-pure-white">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-playfair text-4xl md:text-5xl mb-6 text-pure-black">Certificações & Reconhecimentos</h2>
            </div>
            
            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="bg-pure-black p-8 rounded-2xl text-center transform transition-all hover:scale-[1.02]">
                    <div class="w-16 h-16 bg-gold text-pure-black rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-graduation-cap text-2xl"></i>
                    </div>
                    <h3 class="font-playfair text-xl mb-2 text-pure-white">Psicóloga Registrada</h3>
                    <p class="text-gold">CRP ativo - Conselho Regional de Psicologia</p>
                </div>
                
                <div class="bg-pure-black p-8 rounded-2xl text-center transform transition-all hover:scale-[1.02]">
                    <div class="w-16 h-16 bg-gold text-pure-black rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-user-graduate text-2xl"></i>
                    </div>
                    <h3 class="font-playfair text-xl mb-2 text-pure-white">Pós-graduação</h3>
                    <p class="text-gold">Psicologia Positiva</p>
                </div>
                
                <div class="bg-pure-black p-8 rounded-2xl text-center transform transition-all hover:scale-[1.02]">
                    <div class="w-16 h-16 bg-gold text-pure-black rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-medal text-2xl"></i>
                    </div>
                    <h3 class="font-playfair text-xl mb-2 text-pure-white">Especialista em Desenvolvimento Humano</h3>
                    <p class="text-gold">Certificação Internacional</p>
                </div>
                
                <div class="bg-pure-black p-8 rounded-2xl text-center transform transition-all hover:scale-[1.02]">
                    <div class="w-16 h-16 bg-gold text-pure-black rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-book text-2xl"></i>
                    </div>
                    <h3 class="font-playfair text-xl mb-2 text-pure-white">Coautora</h3>
                    <p class="text-gold">"Quais de mim você procura - Mulheres na Beleza"</p>
                </div>
                
                <div class="bg-pure-black p-8 rounded-2xl text-center transform transition-all hover:scale-[1.02]">
                    <div class="w-16 h-16 bg-gold text-pure-black rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-hands-helping text-2xl"></i>
                    </div>
                    <h3 class="font-playfair text-xl mb-2 text-pure-white">Projetos Sociais</h3>
                    <p class="text-gold">Café das Marias - Prevenção à violência de gênero</p>
                </div>
                
                <div class="bg-pure-black p-8 rounded-2xl text-center transform transition-all hover:scale-[1.02]">
                    <div class="w-16 h-16 bg-gold text-pure-black rounded-full flex items-center justify-center mx-auto mb-4">
                        <i class="fas fa-certificate text-2xl"></i>
                    </div>
                    <h3 class="font-playfair text-xl mb-2 text-pure-white">Especializações</h3>
                    <p class="text-gold">Comunicação Não Violenta, Inteligência Emocional, Liderança, Gestão do Tempo e Saúde Mental Corporativa</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Depoimentos -->
    <section id="depoimentos" class="relative py-24 bg-gold">
        <div class="section-divider">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M1200 120L0 16.48 0 0 1200 0 1200 120z" class="shape-fill" fill="#000000"></path>
            </svg>
        </div>
        
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-playfair text-4xl md:text-5xl mb-6 text-pure-black">O que dizem meus clientes</h2>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-6xl mx-auto">
                <div class="testimonial-card bg-pure-black p-6 rounded-2xl active">
                    <div class="flex items-center mb-4">
                        <i class="fas fa-quote-left text-3xl text-gold mr-3"></i>
                        <h3 class="font-playfair text-xl text-pure-white">Transformação incrível!</h3>
                    </div>
                    <p class="text-pure-white italic">
                        "O trabalho da Dra. Deise mudou completamente minha vida. Em apenas alguns meses, adquiri clareza de propósito e confiança para alcançar meus objetivos profissionais."
                    </p>
                    <div class="flex items-center mt-4">
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300"></i>
                    </div>
                </div>
                
                <div class="testimonial-card bg-pure-black p-6 rounded-2xl">
                    <div class="flex items-center mb-4">
                        <i class="fas fa-quote-left text-3xl text-gold mr-3"></i>
                        <h3 class="font-playfair text-xl text-pure-white">Simplesmente inspiradora</h3>
                    </div>
                    <p class="text-pure-white italic">
                        "Como líder, sempre busco melhorar minha performance e das minhas equipes. Dra. Deise trouxe soluções práticas e humanizadas que transformaram completamente nossa cultura organizacional."
                    </p>
                    <div class="flex items-center mt-4">
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300 mr-1"></i>
                        <i class="fas fa-star text-yellow-300"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Vídeos -->
    <section id="videos" class="py-24 bg-pure-black">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h2 class="font-playfair text-4xl md:text-5xl mb-6 text-gold">Palestras & Vídeos</h2>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="video-card active">
                    <div class="bg-gold bg-opacity-20 backdrop-blur-sm rounded-2xl overflow-hidden shadow-lg">
                        <div class="h-48 bg-gray-700 rounded-t-2xl flex items-center justify-center">
                            <i class="fab fa-youtube text-6xl text-red-600"></i>
                        </div>
                        <div class="p-6">
                            <h3 class="font-playfair text-xl mb-3 text-pure-white">Como desenvolver liderança humanizada</h3>
                            <p class="text-sm text-pure-white mb-4">Evento internacional de liderança - São Paulo/2025</p>
                            <button class="bg-gold text-pure-black py-2 px-4 rounded-full font-bold text-sm">
                                Ver Vídeo Completo
                            </button>
                        </div>
                    </div>
                </div>
                
                <div class="video-card">
                    <div class="bg-gold bg-opacity-20 backdrop-blur-sm rounded-2xl overflow-hidden shadow-lg">
                        <div class="h-48 bg-gray-700 rounded-t-2xl flex items-center justify-center">
                            <i class="fab fa-youtube text-6xl text-red-600"></i>
                        </div>
                        <div class="p-6">
                            <h3 class="font-playfair text-xl mb-3 text-pure-white">CNV no ambiente corporativo</h3>
                            <p class="text-sm text-pure-white mb-4">Workshop Empresarial - Junho/2025</p>
                            <button class="bg-gold text-pure-black py-2 px-4 rounded-full font-bold text-sm">
                                Ver Vídeo Completo
                            </button>
                        </div>
                    </div>
                </div>
                
                <div class="video-card">
                    <div class="bg-gold bg-opacity-20 backdrop-blur-sm rounded-2xl overflow-hidden shadow-lg">
                        <div class="h-48 bg-gray-700 rounded-t-2xl flex items-center justify-center">
                            <i class="fab fa-youtube text-6xl text-red-600"></i>
                        </div>
                        <div class="p-6">
                            <h3 class="font-playfair text-xl mb-3 text-pure-white">Floreser: despertando seu potencial</h3>
                            <p class="text-sm text-pure-white mb-4">Palestra de lançamento - Abril/2025</p>
                            <button class="bg-gold text-pure-black py-2 px-4 rounded-full font-bold text-sm">
                                Ver Vídeo Completo
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Seção Contato Final -->
    <section id="contato" class="py-24 bg-gold">
        <div class="container mx-auto px-6 text-center max-w-4xl">
            <h2 class="font-playfair text-4xl md:text-5xl mb-8 text-pure-black">Vamos transformar vidas e negócios com clareza, sensibilidade e resultados?</h2>
            <p class="text-xl mb-12 text-pure-black max-w-2xl mx-auto">
                Faça contato agora para consultas, palestras, treinamentos corporativos ou mentorias individuais.
            </p>
            
            <div class="flex flex-wrap justify-center gap-6">
                <a href="https://wa.me/5511958030707" target="_blank" class="bg-pure-black text-gold py-4 px-10 rounded-full font-bold transition-all hover:bg-lightwhite hover:text-pure-black flex items-center gap-3">
                    <i class="fab fa-whatsapp text-xl"></i> WhatsApp
                </a>
                <a href="mailto:deiselucipalestrante@gmail.com" class="bg-pure-black text-gold py-4 px-10 rounded-full font-bold transition-all hover:bg-lightwhite hover:text-pure-black flex items-center gap-3">
                    <i class="fas fa-envelope text-xl"></i> Enviar E-mail
                </a>
            </div>
            
            <div class="mt-16 bg-pure-black bg-opacity-30 backdrop-blur p-6 rounded-2xl inline-block">
                <h3 class="font-playfair text-xl mb-4 text-pure-black">Atendimento Local</h3>
                <p class="text-pure-black flex items-center justify-center gap-2">
                    <i class="fas fa-map-marker-alt"></i> Rua Alto Pajeú, 91 – CEP 03726-200
                </p>
                <p class="text-pure-black flex items-center justify-center gap-2 mt-2">
                    <i class="fas fa-calendar-alt"></i> Segunda a sábado – 08h às 18h
                </p>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer class="bg-pure-black py-16 text-center">
        <div class="container mx-auto px-6">
            <!-- Instagram como elemento central -->
            <div class="mb-8">
                <a href="https://www.instagram.com/p/CtMFTzgOSOV/?igsh=MXFpc3N6cjBvZjdsNQ==" target="_blank" class="inline-block bg-gradient-to-r from-purple-500 to-pink-500 p-3 rounded-full">
                    <i class="fab fa-instagram text-pure-white text-2xl"></i>
                </a>
                <p class="mt-4 text-pure-white">Siga no Instagram</p>
            </div>
            
            <div class="mb-8">
                <a href="https://www.instagram.com/dra.deiseluci" target="_blank" class="text-gold text-lg hover:text-pure-white">@dra.deiseluci</a>
            </div>
            
            <div class="mb-8 flex flex-wrap justify-center gap-6">
                <a href="#inicio" class="text-pure-white hover:text-gold">Início</a>
                <a href="#sobre" class="text-pure-white hover:text-gold">Sobre</a>
                <a href="#areas" class="text-pure-white hover:text-gold">Áreas de Atuação</a>
                <a href="#programas" class="text-pure-white hover:text-gold">Programas</a>
                <a href="#saude" class="text-pure-white hover:text-gold">Saúde Mental</a>
                <a href="#certificacoes" class="text-pure-white hover:text-gold">Certificações</a>
                <a href="#depoimentos" class="text-pure-white hover:text-gold">Depoimentos</a>
                <a href="#videos" class="text-pure-white hover:text-gold">Vídeos</a>
                <a href="#contato" class="text-pure-white hover:text-gold">Contato</a>
            </div>
            
            <div class="text-sm text-gray-500">
                <p class="mb-1">© 2025 Dra. Deise Luci - Psicóloga e Especialista em Desenvolvimento Humano</p>
                <p>Site desenvolvido pela <strong>X7</strong></p>
            </div>
        </div>
    </footer>

    <script>
        // Função para as frases rotativas no início
        const phrases = [
            "Agente Transformadora de Vidas",
            "Psicologia e Desenvolvimento Humano",
            "Educação e Saúde Mental",
            "Transformando vidas e negócios"
        ];
        
        let currentPhrase = 0;
        const rotatingElement = document.getElementById('rotating-phrase');
        
        function rotatePhrase() {
            rotatingElement.classList.remove('fade-in');
            rotatingElement.classList.add('fade-out');
            
            setTimeout(() => {
                currentPhrase = (currentPhrase + 1) % phrases.length;
                rotatingElement.textContent = phrases[currentPhrase];
                rotatingElement.classList.remove('fade-out');
                rotatingElement.classList.add('fade-in');
            }, 500);
        }
        
        setInterval(rotatePhrase, 3000);
        
        // Menu Mobile
        document.getElementById('menu-toggle').addEventListener('click', function() {
            document.getElementById('menu-items').classList.toggle('hidden');
            document.getElementById('menu-items').classList.toggle('flex');
        });
        
        // Navegação suave para âncoras
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                
                // Fechar menu mobile após click
                if(window.innerWidth < 768) {
                    document.getElementById('menu-items').classList.add('hidden');
                }
            });
        });
        
        // Mudar menu quando scroll
        window.addEventListener('scroll', function() {
            const nav = document.getElementById('navigation');
            if(window.scrollY > 100) {
                nav.classList.add('py-3', 'shadow-lg', 'bg-opacity-100');
            } else {
                nav.classList.remove('py-3', 'shadow-lg', 'bg-opacity-100');
            }
        });
        
        // Mini efeito para os cards de testemunhos (poderia ser mais elaborado)
        const testimonialCards = document.querySelectorAll('.testimonial-card');
        setInterval(() => {
            testimonialCards.forEach(card => card.classList.remove('active'));
            
            const randomCard = testimonialCards[Math.floor(Math.random() * testimonialCards.length)];
            randomCard.classList.add('active');
        }, 8000);
    </script>
</body>
</html>
