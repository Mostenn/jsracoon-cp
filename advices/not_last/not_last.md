# Применение стилей ко всем элементам, кроме последнего
Используйте CSS `:not()` вместо применения и отмены стилей. Например, хорошо подойдет для навигации, где не надо применять стили для последнего элемента:
```scss
// отмена стилей для последнего элемента
.nav-item {
	border-right: 1px solid #ccc;
	&:last-child {
		border-right: 0;
	}
}

// применение стилей без отмены
.nav-item {
	&:not(:last-child) {
		border-right: 1px solid #ccc;
	}
}
```