# win-rev-shell
We start by generating the payload by using 'msfvenom' 
![image](https://github.com/FireBotato/win-rev-shell/assets/114668318/4b4b7e80-bef3-4ec1-a5b5-358be3566de8) <be>

We run the Apache web server on our machine <br>
![Pasted image 20240522190624](https://github.com/FireBotato/win-rev-shell/assets/114668318/b9ce4e82-2060-471b-8e85-b5dd90818a79) <br>
Then we upload it into the web server we're running <br>
![Pasted image 20240522190143](https://github.com/FireBotato/win-rev-shell/assets/114668318/eac11243-d91b-4f4b-8d71-78a79c88d7c8) <br>
![Pasted image 20240522190208](https://github.com/FireBotato/win-rev-shell/assets/114668318/75e1b65e-fd86-4c3d-9390-65e26adc0683) <br>
then download the payload from the web server running on the Kali machine<br>
![Pasted image 20240522190803](https://github.com/FireBotato/win-rev-shell/assets/114668318/fe2b2c9a-24cd-441e-ba72-68cc91cf4bfe) <br>
we set up the handler on msfconsole so we can listen for a TCP reverse shell when it runs <br>
![Pasted image 20240522191342](https://github.com/FireBotato/win-rev-shell/assets/114668318/5bca2aa2-27c1-4129-82ca-e27e30b16cbd) <br>
![Pasted image 20240522192431](https://github.com/FireBotato/win-rev-shell/assets/114668318/e605a2ce-05c3-487f-ba26-d60f07cefbee) <br>
and when the Windows user runs the payload.exe file we have a reverse TCP shell running (we will use this reverse TCP shell to upload the other payload to the startup file so we can have a persistent back door) <br>
![Pasted image 20240522192523](https://github.com/FireBotato/win-rev-shell/assets/114668318/a29d2816-b062-494d-9058-72efa022e907) <br>
we generate another payload so we can upload it to the startup file <br>
![Pasted image 20240522192658](https://github.com/FireBotato/win-rev-shell/assets/114668318/553a4a44-fcae-42b2-8a68-0e148b2b10bb) <br>
upload the executable to the target machine <br>
![Pasted image 20240522192736](https://github.com/FireBotato/win-rev-shell/assets/114668318/a73a2398-0589-452f-8235-b82fd4bac362) <br>
and move it to the startup file <br>
![Pasted image 20240522193512](https://github.com/FireBotato/win-rev-shell/assets/114668318/792bc651-91d2-47dc-891e-5de94f0968a2) <br>
![Pasted image 20240522193429](https://github.com/FireBotato/win-rev-shell/assets/114668318/79df52e7-056b-4850-8764-df2a6931c877) <br>
then restart the target machine while we have the listener open on msfconsole <br>
![Pasted image 20240522193702](https://github.com/FireBotato/win-rev-shell/assets/114668318/acc6ad13-fd64-4b21-abb5-7cc828a5c7c7) <br>
![Pasted image 20240522193832](https://github.com/FireBotato/win-rev-shell/assets/114668318/b7e41e8d-6548-4fc7-94ef-4e3d50b9b7fb) <br>
so every time the machine restarts the startup.exe payloads run and we can have a reverse TCP shell <br>

![Pasted image 20240522193945](https://github.com/FireBotato/win-rev-shell/assets/114668318/6249315b-3207-4e47-a4c8-17aab5f4fec0)









