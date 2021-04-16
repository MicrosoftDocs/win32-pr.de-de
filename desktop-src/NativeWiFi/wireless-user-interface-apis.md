---
description: Windows 8, Windows Server 2012 und höher enthalten eine neue Verbindungs-Manager-Funktion, mit der Benutzer problemlos eine Verbindung mit dem Internet und anderen Netzwerken (z. b. Arbeits-und Heim Netzwerken) herstellen können.
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: APIs für drahtlose Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5814ea8daa55ab3ec1bf431543174cf57fdfa7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530296"
---
# <a name="wireless-user-interface-apis"></a>APIs für drahtlose Benutzeroberflächen

Windows 8, Windows Server 2012 und höher enthalten eine neue Verbindungs-Manager-Funktion, mit der Benutzer problemlos eine Verbindung mit dem Internet und anderen Netzwerken (z. b. Arbeits-und Heim Netzwerken) herstellen können. Diese neue Verbindungs-Manager-Funktion ersetzt die ältere Verbindung mit **einem Netzwerk** und die Benutzeroberflächen von **Drahtlos Netzwerken** , die in älteren Versionen von Windows zum Verwalten nativer WLAN-Verbindungen enthalten sind.

Unter Windows 7, Windows Server 2008 und Windows Vista gibt es eine Reihe von Benutzeroberflächen (User Interfaces, UIs), die zum Herstellen einer Verbindung mit oder zum Konfigurieren eines drahtlos Netzwerks verwendet werden. Diese Benutzerkonten können in einer Anwendung mit nativen WiFi-und Windows-Shellfunktionen gestartet werden. Diese UIS sind unter Windows 8, Windows Server 2012 und höher nicht verfügbar.

**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Sie können keine Benutzeroberfläche starten, um eine Verbindung mit einem Drahtlos Netzwerk in einer Anwendung Programm gesteuert herzustellen oder ein Drahtlos Netzwerk zu konfigurieren.

## <a name="connect-to-a-network"></a>Herstellen einer Verbindung mit einem Netzwerk

Unter Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 und Windows Vista kann der Assistent **zum Herstellen** einer Verbindung mit einem Netzwerk verwendet werden, um eine Verbindung mit einem Drahtlos Netzwerk herzustellen. Sie können die [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -Funktion verwenden, um den Assistenten zum **Herstellen einer Verbindung mit einem Netzwerk** zu starten.

Der folgende Code zeigt einen [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -Befehl, der den Assistenten zum **Herstellen einer Verbindung mit einem Netzwerk** startet.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

void wmain()
{
   ShellExecute(
      NULL, 
      L"open", 
      L"shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}\\::{38a98528-6cbf-4ca9-8dc0-b1e1d10f7b1b}",
      NULL,
      NULL,
      SW_SHOWNORMAL);
}
```



## <a name="manage-wireless-networks"></a>**Verwalten von Drahtlos Netzwerken**

Unter Windows 7, Windows Server 2008 und Windows Vista wird das System Steuerungselement **drahtlose Netzwerke verwalten** zum Verwalten von Drahtlos Netzwerk Profilen verwendet. Die [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -Funktion kann auch verwendet werden, um das Element " **Drahtlos Netzwerke verwalten** " zu starten. Der Pfad für den Aufruf von **ShellExecute** unter Windows 7 und Windows Vista lautet wie folgt:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

Der folgende Beispielcode zeigt, wie Sie mit [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) den Assistenten für **verwaltete drahtlose Netzwerke** in einer Anwendung starten.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>
#include <stdio.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    HINSTANCE nResult;

    PCWSTR lpOperation = L"open";    
    PCWSTR lpFile= 
        L"shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\\3\\::{1fa9085f-25a2-489b-85d4-86326eedcd87}";

    nResult = ShellExecute(
        NULL,   // Hwnd
        lpOperation, // do not request elevation unless needed
        lpFile,
        NULL, // no parameters 
        NULL, // use current working directory 
        SW_SHOWNORMAL);

    if((int)nResult == SE_ERR_ACCESSDENIED)
    {
        wprintf(L"ShellExecute returned access denied\n");
        wprintf(L"  Executing the ShellExecute command elevated\n"); 

        nResult = ShellExecute(
            NULL,
            L"runas", // Trick for requesting elevation
            lpFile,
            NULL, // no parameters 
            NULL, // use current working directory 
            SW_HIDE);
    }

    if ( (int) nResult < 32) {
        wprintf(L" ShellExecute failed with error %d\n", (int) nResult);
        return 1;
    }    
    else {    
        wprintf(L" ShellExecute succeeded and returned value %d\n", (int) nResult);
        return 0;
    }
}

```



## <a name="advanced-settings-for-wireless-network-profiles"></a>Erweiterte Einstellungen für Drahtlos Netzwerk Profile

Windows Vista und höher enthalten eine erweiterte Benutzeroberfläche, die verwendet wird, um erweiterte Einstellungen eines Drahtlos Netzwerk Profils anzuzeigen und zu bearbeiten. Sie können diese erweiterte Benutzeroberfläche starten, indem Sie die [**wlanuieditprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) -Funktion aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von nativem WiFi](using-native-wifi.md)
</dt> <dt>

[Beispiele für Funk profile](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**Wlanuieditprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
