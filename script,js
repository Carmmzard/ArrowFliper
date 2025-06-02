const coin = document.getElementById('coin');
const flipButton = document.getElementById('flip-button');
const result = document.getElementById('result');

flipButton.addEventListener('click', () => {
    // Отключаем кнопку во время анимации
    flipButton.disabled = true;
    
    // Сбрасываем результат и классы анимации
    result.textContent = '';
    coin.classList.remove('flipping-heads', 'flipping-tails');
    
    // Небольшая задержка для сброса анимации перед повторным запуском
    setTimeout(() => {
        // Определяем результат (true для Орла, false для Решки)
        const isHeads = Math.random() < 0.5;
        
        // Запускаем соответствующую анимацию
        requestAnimationFrame(() => {
            if (isHeads) {
                coin.classList.add('flipping-heads');
            } else {
                coin.classList.add('flipping-tails');
            }
        });
        
        // После завершения анимации (длительность 1000мс)
        setTimeout(() => {
            // Показываем результат
            if (isHeads) {
                result.textContent = 'Выпал Орёл!';
            } else {
                result.textContent = 'Выпала Решка!';
            }
            
            // Включаем кнопку обратно
            flipButton.disabled = false;
        }, 1000);
    }, 50); // Небольшая задержка (например, 50 мс) для сброса анимации
});

// Функционал для галереи
document.querySelectorAll('.gallery-item').forEach(item => {
    item.addEventListener('click', () => {
        const isBanned = item.classList.toggle('banned');
        const overlay = item.querySelector('.ban-overlay');
        overlay.textContent = isBanned ? 'Unban' : 'Ban';
    });
}); 
