<template>
	<div class="xue_comp_gradeBox">
	    <div class="xue_comp_gradeBox_shadow">
	        <div class="xue_comp_gradeBox_main big">
	            <div>
	                <p class="main_title">请选择孩子在校的真实年级</p>
	                <ul class="main_list_box clearfix">
	                    <li class="main_list"></li>
	                </ul>
	            </div>
	        </div>
	    </div>
	</div>
</template>

<script>
	export default {

	}
</script>

<style scoped lang="scss">
	.xue_comp_gradeBox {
		position: fixed;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
		.xue_comp_gradeBox_shadow {
			background: rgba(0, 0, 0, 0.6);
			position: absolute;
			width: 100%;
			height: 100%;
			left: 0;
			top: 0;
		}
		.xue_comp_gradeBox_data {
			@include animate(showAlert, .3s, '');
			width: px2rem(670);
			padding-bottom: px2rem(15);
			background: #fff;
			position: absolute;
			left: 50%;
			top: 18%;
			margin-left: px2rem(-335);
			border-radius: px2rem(40);
			overflow: hidden;
			.gradeBox_close {
				position: absolute;
				right: 0;
				top: 0;
				width: px2rem(108);
				height: px2rem(108);
				background: url(#{$img}center/close.png) no-repeat center center;
				background-size: px2rem(23) px2rem(23);
			}
			.gradeBox_header {
				height: px2rem(108);
				border-bottom: 1px solid #CCCCCC;
				font-size: px2rem(30);
				line-height: px2rem(108);
				text-align: center;
				color: #212121;
			}
		}
	}

	.xue_comp_gradeBox_main {
		padding: px2rem(64) 0 0 px2rem(55);
		width: 100%;
		box-sizing: border-box;
		background: #fff;
		&.big .main_list_box .main_list {
			width: px2rem(180);
		}
		.main_title {
			font-size: px2rem(26);
			line-height: px2rem(26);
			margin-bottom: px2rem(30);
			color: #BDBDBD;
		}
		.main_list_box {
			margin-bottom: px2rem(10);
			.main_list {
				float: left;
				width: px2rem(160);
				height: px2rem(60);
				color: #6F6F6F;
				font-size: px2rem(30);
				line-height: px2rem(60);
				box-sizing: border-box;
				border: 1px solid #BDBDBD;
				text-align: center;
				border-radius: px2rem(30);
				margin-right: px2rem(40);
				margin-bottom: px2rem(60);
				&.on {
					color: #F95862;
					border: 1px solid #F95862;
				}
			}
		}
	}
</style>