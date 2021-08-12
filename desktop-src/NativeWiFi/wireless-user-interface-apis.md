---
description: Windows 8, Windows Server 2012 und höher enthalten ein neues Verbindungs-Manager-Feature, mit dem Benutzer problemlos eine Verbindung mit dem Internet und anderen Netzwerken (z. B. Arbeits- und Heimnetzwerken) herstellen können.
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: APIs Benutzeroberfläche drahtlosen Verbindungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2b2af7faccc5452163ad89ed28d12e7de917f4b872011165e0cfb1760657dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619927"
---
# <a name="wireless-user-interface-apis"></a>APIs Benutzeroberfläche drahtlosen Verbindungen

Windows 8, Windows Server 2012 und höher enthalten ein neues Verbindungs-Manager-Feature, mit dem Benutzer problemlos eine Verbindung mit dem Internet und anderen Netzwerken (z. B. Arbeits- und Heimnetzwerken) herstellen können. Dieses neue Verbindungs-Manager ersetzt die älteren **Verbinden** in ein  Netzwerk und die Benutzeroberflächen von Drahtlosen Netzwerken verwalten, die in älteren Versionen von Windows für die Verwaltung von Native Wifi-Verbindungen enthalten sind.

In Windows 7, Windows Server 2008 und Windows Vista gibt es eine Reihe von Benutzeroberflächen (UIs), die zum Herstellen einer Verbindung mit einem Drahtlosnetzwerk oder zum Konfigurieren eines Drahtlosnetzwerks verwendet werden. Diese Beis können in einer Anwendung mit nativem WLAN und Windows Shell-Funktionen gestartet werden. Diese Beis sind nicht für Windows 8, Windows Server 2012 und höher verfügbar.

**Windows XP mit SP3 und der Wlan-LAN-API für Windows XP mit SP2:** Sie können keine Benutzeroberfläche starten, die zum herstellen oder programmgesteuerten Konfigurieren eines Drahtlosnetzwerks in einer Anwendung verwendet wird.

## <a name="connect-to-a-network"></a>Herstellen einer Verbindung mit einem Netzwerk

In Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 und Windows Vista kann der **Assistent Verbinden** zu einem Netzwerk verwendet werden, um eine Verbindung mit einem Drahtlosnetzwerk herzustellen. Sie können die [**ShellExecute-Funktion**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) verwenden, um die Verbinden **Netzwerk-Assistenten zu** starten.

Der folgende Code zeigt einen [**ShellExecute-Aufruf,**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) der die Verbinden **netzwerk-Assistenten** startet.


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



## <a name="manage-wireless-networks"></a>**Verwalten von Drahtlosnetzwerken**

Unter Windows 7, Windows Server 2008 und Windows Vista wird  das Systemsteuerung-Element Drahtlosnetzwerke verwalten zum Verwalten von Drahtlosnetzwerkprofilen verwendet. Die [**ShellExecute-Funktion**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) kann auch verwendet werden, um das Element Drahtlose Netzwerke **verwalten zu** starten. Der Pfad, der beim Aufrufen von **ShellExecute** auf Windows 7 und Windows Vista verwendet werden soll, ist der folgende:

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

Der folgende Beispielcode zeigt, wie [**ShellExecute verwendet**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) wird, um den Assistenten für verwaltete **Drahtlosnetzwerke** aus einer Anwendung zu starten.


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



## <a name="advanced-settings-for-wireless-network-profiles"></a>Erweiterte Einstellungen für Drahtlosnetzwerkprofile

Windows Vista und höher enthalten eine erweiterte Benutzeroberfläche, die zum Anzeigen und Bearbeiten erweiterter Einstellungen eines Drahtlosnetzwerkprofils verwendet wird. Sie können diese erweiterte Benutzeroberfläche starten, indem Sie die [**WlanUIEditProfile-Funktion**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von nativem WLAN](using-native-wifi.md)
</dt> <dt>

[Beispiele für Drahtlosprofile](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WLANUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
