
Напишите валидационный скрипт используя функции 

 1. Скрипт должен на вход принимать строку.
 2. После проверки строки выводить в консоль сообщение где будет конкретно написано, что не так в ведённой строке.
 3. Минимум 5 символов в строке
 4. Максимум 64 символа в строке
 5. В строке должны быть буквы
 6. Должна быть хотя бы одна буква в верхнем регистре
 7. Должна быть хотя бы одна цифра
 8. Должна быть хотя бы одна @
 9. Строка не должна быть пустой
const validateString = function(inputString)
 {
 
if (inputString.trim() === "")

{ console.log("Ошибка: Строка не должна быть пустой.");
return;

}
    
if (inputString.length < 5)
{
console.log("Ошибка: Минимум 5 символов в строке.");
return;

}

if (inputString.length > 64) 
{

console.log("Ошибка: Максимум 64 символа в строке.");
return;
}

if (!/[a-zA-Z]/.test(inputString)) {
console.log("Ошибка: В строке должны быть буквы.");
return;

}

if (!/[A-Z]/.test(inputString)) 
{

console.log("Ошибка: Должна быть хотя бы одна буква в верхнем регистре.");
return;

}

if (!/\d/.test(inputString))

{
console.log("Ошибка: Должна быть хотя бы одна цифра.");
return;

}
if (!/@/.test(inputString))
{

console.log("Ошибка: Должна быть хотя бы одна '@'.");
return;
}

console.log("Строка прошла валидацию успешно!");
};

validateString("Hello123@"); 
validateString("Hello");      
validateString("12345");      
validateString("Hello@");    
validateString("hello123@");  
validateString("");         
