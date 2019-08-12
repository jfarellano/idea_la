<template lang='pug'>

div.container-fluid.main
	section.row.justify-content-center
		div.col-md-10.align-self-center
			div.out-box
				div.in-box.container-fluid
					div.bulb
						img(src="../assets/bulb.svg")
					div.row.align-items-center
						div.col
							img(src="../assets/logo.svg" )
							h4 Tú lo imaginas, nosotros lo hacemos realidad
	section.row.justify-content-center.align-items-center.we
		div.col-md-5
			div.image
				img(src='../assets/people.svg')
				div.line
		div.col-md-7
			h2 Todos para uno y uno para todos
			p Somos un grupo de desarrollo conformado por <a target='_blank' href='https://github.com/jfarellano'>Juan Arellano</a>, <a target='_blank' href='https://github.com/JohnDBR'>John Barbosa</a>, <a target='_blank' href='https://github.com/aconchatorres'>Andrés Concha</a> y <a target='_blank' href='https://github.com/onailimixam'>Max García</a>. Compañeros desde hace cuatro años en la universidad y proyectos. Nos especializamos en desarrollo Web y Android siempre buscando llevar las mejores practicas y las tecnologías mas modernas para brindar soluciones a tus ideas
	section.row.justify-content-end.products
		//- div.scroller(@click="scrollSide()")
		//- 	img(src='../assets/arrow.svg')
		div.col-11.align-self-center(style="padding-right: 0px;")
			div.list-container.container-fluid
				div.row.flex-row.flex-nowrap
					div.info.col.align-self-center
						h3 Nuestro Trabajo
						p Estos son algunos proyectos en los que los miembros del grupo han trabajado
					div.product-card.col
						div.container-fluid
							div.row.image
								img(src='../assets/projects/ciuda.png')
							div.row.data
								div.col
									h5 Imagina tu Ciudá
									p Se Desarrollo una aplicación web para la Cámara de Comercio de Barranquilla la cual busca la participación ciudadana mediante un espacio de co-creación entre ciudadanía y gobernantes. Esta plataforma fue desarrollada en Vue.JS y Ruby on Rails 
									button(@click="toSite('ciuda')") Conoce este proyecto
					div.product-card.col
						div.container-fluid
							div.row.image
								img(src='../assets/projects/nomit.png')
							div.row.data
								div.col
									h5 Nomit
									p NOMIT te conecta a la comunidad de conductores de tu ciudad. Con esta aplicación estás SIEMPRE informado de lo que está pasando en las vías. John hizo parte del equipo de desarrollo de esta aplicación Android.
									button(@click="toSite('nomit')") Conoce este proyecto
					div.product-card.col
						div.container-fluid
							div.row.image
								img(src='../assets/projects/litivo.png')
							div.row.data
								div.col
									h5 Litivo
									p Litivo es una aplicación web en la cual la ciudadanía puede ejercer procesos de conciliación y de insolvencia mediante la Fundación Liborio Mejía de manera totalmente digital y llevando todas las constancias de los procesos en la plataforma. Juan hizo parte del equipo de desarrollo del front-end de esta aplicación en Angular.js
									button(@click="toSite('litivo')") Conoce este proyecto
					div.product-card.col
						div.container-fluid
							div.row.image
								img(src='../assets/projects/pasuu.png')
							div.row.data
								div.col
									h5 Pasuu
									p Pasuu te brinda información de por donde puedes desplazarte con menor probabilidad de hurto en zonas que no conoces. En el equipo de desarrollo de esta app Android John hizo parte
									button(@click="toSite('pasuu')") Conoce este proyecto
					div.separator.col

	div.row.contact-section
		div.col(align="center")
			h1 Contacto
			b-form(method="POST" action="https://formspree.io/info@idea-la.com")
				b-input.input-field(type="text" name="name" placeholder="Nombre")
				b-input.input-field(type="email" name="email" placeholder="Correo")
				b-input.input-field(type="text" name="company" placeholder="Compañía")
				b-textarea.input-field(name="message" placeholder="Mensaje")
				b-button.send-button(type="submit") Enviar
        
</template>

<script>
export default {
  methods: {
    scrollSide() {
      let content = document.querySelector(".list-container");
      content.scrollLeft += 40;
    },
    toSite(name){
      switch (name) {
        case 'ciuda':
          window.open('https://www.imaginatuciuda.org','_blank');
          break;
        case 'nomit':
          window.open('https://play.google.com/store/apps/details?id=nomit.mobile.android&hl=en', '_blank')
          break;
        case 'litivo':
          window.open('https://www.litivo.com', '_blank')
					break;
				case 'pasuu':
          window.open('https://play.google.com/store/apps/details?id=pasuu.pasuu.android&hl=en', '_blank')
          break;
        default:
          break;
      }
    }
  }
};
</script>

<style scoped lang='scss'>
.main {
  background-color: #ffe01b;
  section {
    min-height: 70vh;
  }
	.contact-section {
		padding-bottom: 20px;
		.input-field {
			max-width: 700px;
			margin-bottom: 10px;
		}
    .send-button {
      width: 100px;
      background-color: black
    }
	}
  .out-box {
    height: 50vh;
    padding: 10px;
    text-align: center;
    background-color: white;
    .in-box {
      height: 100%;
      border: 1.5px solid black;
      position: relative;
      .bulb {
        position: absolute;
        left: 50px;
        bottom: -1.5px;
        img {
          position: relative;
          width: 80px;
          z-index: 1000;
        }
      }
      .row {
        height: 100%;
        img {
          width: 60%;
        }
      }
    }
  }
  .we {
    text-align: center;
    overflow: hidden;
    .image {
      position: relative;
      img {
        position: relative;
        width: 350px;
        z-index: 1000;
      }
      .line {
        position: absolute;
        bottom: 33px;
        left: -1000px;
        height: 2px;
        background-color: #4d4d4d;
        width: 100000px;
      }
    }
    h2 {
      font-weight: bold;
    }
    h2,
    p {
      padding-right: 20px;
      direction: rtl;
      text-align: justify;
    }
    a{
      color: #4d4d4d;
      font-weight: bold;
    }
  }
  .products {
    position: relative;
    .scroller {
      z-index: 1000;
      background-color: #ffe01b;
      position: absolute;
      right: 0px;
      top: 50%;
      padding: 3px 10px;
      img {
        width: 70px;
      }
    }
    .list-container {
      overflow-x: auto;
      background-color: white;
      height: 440px;
      padding: 25px 0px;
      .info.col {
        flex-grow: unset;
        display: inline-block;
        width: 150px;
        margin: 0px 30px;
      }
      .separator {
        display: inline-block;
        background-color: white;
        width: 300px;
        height: 200px;
      }
      .product-card {
        display: inline-block;
        padding: 0px;
        margin: 0px 10px;
        width: 280px;
        height: 400px;
        border: 2px #4d4d4d solid;
        &:last-of-type {
          margin-right: 150px;
        }
        .data {
          padding: 10px;
          h5{
            color: black;
          }
          p {
            font-size: 10px;
            text-align: justify;
          }
          button {
            height: 30px;
            background-color: transparent;
            border: 2px #4d4d4d solid;
            outline-color: #ffe01b;
            outline-style: solid;
            outline-width: 1px;
            outline-offset: 0.5px;
            font-size: 10px;
            width: 100%;
          }
        }
      }
    }
  }
}
</style>

