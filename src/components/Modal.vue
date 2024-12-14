<template>
  <div class="card-modal-overlay" :class="{open: isOpen}" @click.self="closeModal">
            <div class="card-modal">
                <div class="card-modal-header">
                    <h2 class="card-modal-header-title">Корзина</h2>
                    <span class="card-modal-header-close" @click="closeModal">
                        <img src="../assets/images/icon/close.png" alt="close">
                    </span>
                </div>
                <div class="card-modal-body">
                    <div class="card-modal-body-item">
                        <p class="card-modal-body-title">Ролл угорь стандарт</p>
                        <div class="card-modal-body-item-controls">
                            <div class="card-modal-body-item-controls-price">250 ₽</div>
                            <button class="btn-quantity">-</button>
                            <div class="card-item-controls-count">1</div>
                            <button class="btn-quantity">+</button>
                        </div>
                    </div>
                    <div class="card-modal-body-item">
                        <p class="card-modal-body-title">Ролл угорь стандарт</p>
                        <div class="card-modal-body-item-controls">
                            <div class="card-modal-body-item-controls-price">250 ₽</div>
                            <button class="btn-quantity">-</button>
                            <div class="card-item-controls-count">1</div>
                            <button class="btn-quantity">+</button>
                        </div>
                    </div>
                    <div class="card-modal-body-item">
                        <p class="card-modal-body-title">Ролл угорь стандарт</p>
                        <div class="card-modal-body-item-controls">
                            <div class="card-modal-body-item-controls-price">250 ₽</div>
                            <button class="btn-quantity">-</button>
                            <div class="card-item-controls-count">1</div>
                            <button class="btn-quantity">+</button>
                        </div>
                    </div>
                </div>
                <div class="card-modal-footer">
                    <div class="card-modal-footer-price">
                        1250 ₽
                    </div>
                    <div class="card-modal-footer-controls">
                        <button class="btn btn-primery">Оформить заказ</button>
                        <button class="btn btn-outline">Отмена</button>
                    </div>
                </div>
            </div>
        </div>
</template>

<script setup>

    const {isOpen} = defineProps({isOpen: Boolean})
    const emit = defineEmits(['toggleModal']);
    const closeModal = () => emit('toggleModal')   
    
 
</script>

<style scoped>
.card-modal-overlay {
    display: none;
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    align-items: center;
    justify-content: center;
    background: rgba(0, 0, 0, 0.45);
}

.card-modal-overlay.open {
    display: flex;
}

.card-modal {
    width: 100%;
    max-width: 780px;
    border-radius: 5px;
    padding: 40px 45px;
    background: #FFF;

}

.card-modal-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 48px;
}

.card-modal-header-title {
    margin: 0;
    font-weight: 700;
    font-size: 36px;
    color: #000;
}

.card-modal-header-close {
    cursor: pointer;
}

.card-modal-body-item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;


}

.card-modal-body-item:not(:last-child) {
    padding-bottom: 10x;
    margin-bottom: 17px;
    border-bottom: 1px solid #d9d9d9;
}

.card-modal-body-title {
    font-weight: 400;
    font-size: 18px;
    line-height: 178%;
    color: #8c8c8c;
    margin: 0;
}

.card-modal-body-item-controls {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
}

.card-modal-body-item-controls-price {
    font-size: 20px;
    line-height: 160%;
    color: #000;
    margin: 0;
    margin-right: 47px;
}

.btn-quantity {
    border: 1px solid #1890ff;
    border-radius: 2px;

    width: 36px;
    height: 32px;
    background: #FFF;
    color: #1890ff;
}



.card-item-controls-count {
    margin-left: 15px;
    margin-right: 15px;
    font-weight: 400;
    font-size: 16px;
    line-height: 150%;
    text-align: center;
    color: #262626;
}

.card-modal-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 50px;
}

.card-modal-footer-price {
    border-radius: 5px;
    padding: 15px 20px;
    width: 106px;
    font-weight: 700;
    font-size: 20px;
    color: #FFF;
    background: #302c34;
}

.card-modal-footer-controls {
    display: flex;
    align-items: center;
    gap: 10px;
}
</style>