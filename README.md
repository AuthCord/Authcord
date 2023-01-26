<font size="24">
<div align="center">
 HWID Based Authentication made Simple. Find out more here: <a href="https://authcord.xyz"> authcord.xyz </a>
</div>
</font>

<div align="center" >
 Examples using Authcord:
</div>

<a href="https://github.com/AuthCord/authcord-cpp"> Using Authcord in CPP: </a>
```
using namespace Authcord;
std::string apiKey = XorStr("yourkey");
std::string adminKey = XorStr("yourkey");
API AuthcordApp(apiKey, adminKey);

int main()
{
	SetConsoleTitleA(skCrypt("Authcord Loader"));
	system(skCrypt("cls"));

	AuthcordApp.Init(apiKey);
	std::cout << XorStr("\n Connecting....") << std::endl;

	AuthcordApp.Login(apiKey);
	system(skCrypt("cls"));
	std::cout << skCrypt("\n Welcome ") << XorStr("User! B]") << std::endl;
	Sleep(1500);

	system(skCrypt("cls"));
	std::cout << XorStr("\n\n Downloading...") << std::endl;

	std::string urldl = XorStr("https://example.url/example.exe");
	AuthcordApp.Download(urldl, "C:\\example.exe");

	std::cout << XorStr("\n Done!") << std::endl;
	system(skCrypt("cls"));

	//
	//  < Your Code >
	//


	Sleep(5000);

	return 0;

}
```

<a href="https://github.com/AuthCord/authcord-golang"> Using Authcord in Golang: </a>
```
package main

import (
	"authcord"
	"fmt"
)

func main() {
	// get users HWID
	hwid := authcord.GetHWID()
	// Initialize a new Authcord client with your API key
	client := authcord.NewAuthcordClient("YOUR_USER_LEVEL_KEY")

	// Check the HWID of a user
	response, err := client.CheckHWID(hwid)
	if err != nil {
		fmt.Println("Error checking HWID:", err)
		return
	}
	fmt.Println("Response:", response)

}
```
