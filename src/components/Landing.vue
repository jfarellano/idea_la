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
							h4 Tu lo imaginas, nosotros lo hacemos realidad
	section.row.justify-content-center.align-items-center.we
		div.col-md-5
			div.image
				img(src='../assets/people.svg')
				div.line
		div.col-md-7
			h2 Todos para uno y uno para todos
			p Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.
	section.row.justify-content-end.products
		div.scroller(@click="scrollSide()")
			img(src='../assets/arrow.svg')
		div.col-11.align-self-center(style="padding-right: 0px;")
			div.list-container.container-fluid
				div.row.flex-row.flex-nowrap
					div.info.col.align-self-center
						h3 Nuestro Trabajo
						p Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod aliquam erat volutpat.
					div.product-card.col
						div.container-fluid
							div.row.image
								img(src='https://via.placeholder.com/280x150')
							div.row.data
								div.col
									h5 Nombre del producto
									p Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit
									button Conoce este proyecto
					div.product-card.col
						div.container-fluid
							div.row.image
								img(src='https://via.placeholder.com/280x150')
							div.row.data
								div.col
									h5 Nombre del producto
									p Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit
									button Conoce este proyecto
					div.product-card.col
						div.container-fluid
							div.row.image
								img(src='https://via.placeholder.com/280x150')
							div.row.data
								div.col
									h5 Nombre del producto
									p Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit
									button Conoce este proyecto
					div.separator.col 
	
</template>

<script>
export default {
  methods: {
    scrollSide() {
      let content = document.querySelector(".list-container");
      content.scrollLeft += 40;
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
  .out-box {
    height: 50vh;
    padding: 10px;
    text-align: center;
    background-color: white;
    .in-box {
      height: 100%;
      border: 1.5px solid black;
			position: relative;
			.bulb{
				position: absolute;
				left: 50px;
				bottom: -1.5px;
				img{
					position:relative;
					width: 80px;
					z-index: 1000;
				}
			}
      .row {
        height: 100%;
        img {
          width: 350px;
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
			img{
				width: 70px;
			}
    }
    .list-container {
      overflow-x: auto;
      background-color: white;
      height: 400px;
      padding: 25px 0px;
      .info.col {
        flex-grow: unset;
        display: inline-block;
        width: 150px;
        margin: 0px 30px;
      }
			.separator{
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
        height: 350px;
        border: 2px #4d4d4d solid;
				&:last-of-type{
					margin-right: 150px;
				}
        .data {
          padding: 10px;
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

