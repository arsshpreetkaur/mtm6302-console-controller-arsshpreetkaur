document.addEventListener('DOMContentLoaded', function() {
    const bgColorInput = document.getElementById('bg-color');
    const textColorInput = document.getElementById('text-color');
    const fontSizeInput = document.getElementById('font-size');
    const fontFamilySelect = document.getElementById('font-family');
    const textAlignSelect = document.getElementById('text-align');
    const borderStyleSelect = document.getElementById('border-style');
    const applyButton = document.getElementById('apply');
    const resetButton = document.getElementById('reset');

    function applyChanges() {
        const bgColor = bgColorInput.value;
        const textColor = textColorInput.value;
        const fontSize = fontSizeInput.value;
        const fontFamily = fontFamilySelect.value;
        const textAlign = textAlignSelect.value;
        const borderStyle = borderStyleSelect.value;

        document.body.style.backgroundColor = bgColor;
        document.body.style.color = textColor;
        document.body.style.fontSize = fontSize + 'px';
        document.body.style.fontFamily = fontFamily;
        document.body.style.textAlign = textAlign;
        document.body.style.borderStyle = borderStyle;

        console.log('Background Color:', bgColor);
        console.log('Text Color:', textColor);
        console.log('Font Size:', fontSize + 'px');
        console.log('Font Family:', fontFamily);
        console.log('Text Alignment:', textAlign);
    

        saveSettings();
    }

    function resetToDefault() {
        document.body.style.backgroundColor = '';
        document.body.style.color = '';
        document.body.style.fontSize = '';
        document.body.style.fontFamily = '';
        document.body.style.textAlign = '';
        document.body.style.borderStyle = '';

        bgColorInput.value = '#ffffff';
        textColorInput.value = '#000000';
        fontSizeInput.value = 16;
        fontFamilySelect.value = 'Arial';
        textAlignSelect.value = 'left';
        borderStyleSelect.value = 'none';

        localStorage.removeItem('customStyles');
    }

    function saveSettings() {
        const settings = {
            bgColor: bgColorInput.value,
            textColor: textColorInput.value,
            fontSize: fontSizeInput.value,
            fontFamily: fontFamilySelect.value,
            textAlign: textAlignSelect.value,
            borderStyle: borderStyleSelect.value
        };
        localStorage.setItem('customStyles', JSON.stringify(settings));
    }

    function loadSettings() {
        const savedSettings = JSON.parse(localStorage.getItem('customStyles'));
        if (savedSettings) {
            bgColorInput.value = savedSettings.bgColor;
            textColorInput.value = savedSettings.textColor;
            fontSizeInput.value = savedSettings.fontSize;
            fontFamilySelect.value = savedSettings.fontFamily;
            textAlignSelect.value = savedSettings.textAlign;
            borderStyleSelect.value = savedSettings.borderStyle;

            applyChanges();
        }
    }

    applyButton.addEventListener('click', applyChanges);
    resetButton.addEventListener('click', resetToDefault);

    loadSettings();
});
