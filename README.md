##说明

ys-Animate服务是用tween算法为angular.js封装的一套动画实现，由于ng内置的jq-lite仅支持行间样式的获取，所以引用本服务时，必须先给AngularElm设置初始行间样式

##方法

ys-Animate支持常规属性的动画效果以及transform的动画效果

##用法

引入ys-Animate服务之后，直接调取服务下的`move`或者`transform`方法并传入参数即可

    ys-Animate.move({
    	target: { top: 100, left: 100 }, // 目标点
		time: 500, // 所需时间
		fx: 'linear', // 动画方式
		fn: function() { // 回调函数
			alert('a')
		}
    });

    ys-Animate.transform({
    	target: { translate: [100, 100], rotate: 20, scale: [0.8, 1.2] }, // 目标点
		time: 500, // 所需时间
		fx: 'linear', // 动画方式
		fn: function() { // 回调函数
			alert('a')
		}
    });