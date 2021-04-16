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
# <a name="wireless-user-interface-apis"></a><span data-ttu-id="5592c-103">APIs für drahtlose Benutzeroberflächen</span><span class="sxs-lookup"><span data-stu-id="5592c-103">Wireless User Interface APIs</span></span>

<span data-ttu-id="5592c-104">Windows 8, Windows Server 2012 und höher enthalten eine neue Verbindungs-Manager-Funktion, mit der Benutzer problemlos eine Verbindung mit dem Internet und anderen Netzwerken (z. b. Arbeits-und Heim Netzwerken) herstellen können.</span><span class="sxs-lookup"><span data-stu-id="5592c-104">Windows 8, Windows Server 2012, and later include a new Connection Manager feature that allows users to easily connect to the Internet and to other networks (work and home networks, for example).</span></span> <span data-ttu-id="5592c-105">Diese neue Verbindungs-Manager-Funktion ersetzt die ältere Verbindung mit **einem Netzwerk** und die Benutzeroberflächen von **Drahtlos Netzwerken** , die in älteren Versionen von Windows zum Verwalten nativer WLAN-Verbindungen enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="5592c-105">This new Connection Manager feature replaces the older **Connect to a network** and **Manage Wireless Networks** user interfaces included with older versions of Windows for managing Native Wifi connections.</span></span>

<span data-ttu-id="5592c-106">Unter Windows 7, Windows Server 2008 und Windows Vista gibt es eine Reihe von Benutzeroberflächen (User Interfaces, UIs), die zum Herstellen einer Verbindung mit oder zum Konfigurieren eines drahtlos Netzwerks verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5592c-106">On Windows 7, Windows Server 2008, and Windows Vista, there are a number of user interfaces (UIs) used to connect to or configure a wireless network.</span></span> <span data-ttu-id="5592c-107">Diese Benutzerkonten können in einer Anwendung mit nativen WiFi-und Windows-Shellfunktionen gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="5592c-107">These UIs can be started in an application using Native Wifi and Windows Shell functions.</span></span> <span data-ttu-id="5592c-108">Diese UIS sind unter Windows 8, Windows Server 2012 und höher nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5592c-108">These UIs are not available on Windows 8, Windows Server 2012, and later.</span></span>

<span data-ttu-id="5592c-109">**Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2:** Sie können keine Benutzeroberfläche starten, um eine Verbindung mit einem Drahtlos Netzwerk in einer Anwendung Programm gesteuert herzustellen oder ein Drahtlos Netzwerk zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5592c-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** You cannot start any UI used to connect to or configure a wireless network in an application programmatically.</span></span>

## <a name="connect-to-a-network"></a><span data-ttu-id="5592c-110">Herstellen einer Verbindung mit einem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="5592c-110">Connect to a network</span></span>

<span data-ttu-id="5592c-111">Unter Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 und Windows Vista kann der Assistent **zum Herstellen** einer Verbindung mit einem Netzwerk verwendet werden, um eine Verbindung mit einem Drahtlos Netzwerk herzustellen.</span><span class="sxs-lookup"><span data-stu-id="5592c-111">On Windows 8, Windows Server 2012, Windows 7, Windows Server 2008, and Windows Vista, the **Connect to a network** wizard can be used to establish a connection to a wireless network.</span></span> <span data-ttu-id="5592c-112">Sie können die [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -Funktion verwenden, um den Assistenten zum **Herstellen einer Verbindung mit einem Netzwerk** zu starten.</span><span class="sxs-lookup"><span data-stu-id="5592c-112">You can use the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function to start the **Connect to a network** wizard.</span></span>

<span data-ttu-id="5592c-113">Der folgende Code zeigt einen [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -Befehl, der den Assistenten zum **Herstellen einer Verbindung mit einem Netzwerk** startet.</span><span class="sxs-lookup"><span data-stu-id="5592c-113">The following code shows a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) call that starts the **Connect to a network** wizard.</span></span>


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



## <a name="manage-wireless-networks"></a><span data-ttu-id="5592c-114">**Verwalten von Drahtlos Netzwerken**</span><span class="sxs-lookup"><span data-stu-id="5592c-114">**Manage Wireless Networks**</span></span>

<span data-ttu-id="5592c-115">Unter Windows 7, Windows Server 2008 und Windows Vista wird das System Steuerungselement **drahtlose Netzwerke verwalten** zum Verwalten von Drahtlos Netzwerk Profilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5592c-115">On Windows 7, Windows Server 2008, and Windows Vista, the **Manage Wireless Networks** Control Panel item is used to manage wireless network profiles.</span></span> <span data-ttu-id="5592c-116">Die [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) -Funktion kann auch verwendet werden, um das Element " **Drahtlos Netzwerke verwalten** " zu starten.</span><span class="sxs-lookup"><span data-stu-id="5592c-116">The [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function can also be used to start the **Manage Wireless Networks** item.</span></span> <span data-ttu-id="5592c-117">Der Pfad für den Aufruf von **ShellExecute** unter Windows 7 und Windows Vista lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5592c-117">The path to use when calling **ShellExecute** on Windows 7 and Windows Vista is the following:</span></span>

<span data-ttu-id="5592c-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span><span class="sxs-lookup"><span data-stu-id="5592c-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span></span>

<span data-ttu-id="5592c-119">Der folgende Beispielcode zeigt, wie Sie mit [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) den Assistenten für **verwaltete drahtlose Netzwerke** in einer Anwendung starten.</span><span class="sxs-lookup"><span data-stu-id="5592c-119">The following sample code shows how to use [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to start the **Managed Wireless Networks** wizard from an application.</span></span>


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



## <a name="advanced-settings-for-wireless-network-profiles"></a><span data-ttu-id="5592c-120">Erweiterte Einstellungen für Drahtlos Netzwerk Profile</span><span class="sxs-lookup"><span data-stu-id="5592c-120">Advanced Settings for Wireless Network Profiles</span></span>

<span data-ttu-id="5592c-121">Windows Vista und höher enthalten eine erweiterte Benutzeroberfläche, die verwendet wird, um erweiterte Einstellungen eines Drahtlos Netzwerk Profils anzuzeigen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="5592c-121">Windows Vista and later include an advanced user interface that is used to view and edit advanced settings of a wireless network profile.</span></span> <span data-ttu-id="5592c-122">Sie können diese erweiterte Benutzeroberfläche starten, indem Sie die [**wlanuieditprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5592c-122">You can start this advanced UI by calling the [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5592c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5592c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5592c-124">Verwenden von nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="5592c-124">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="5592c-125">Beispiele für Funk profile</span><span class="sxs-lookup"><span data-stu-id="5592c-125">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="5592c-126">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="5592c-126">**ShellExecute**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="5592c-127">**Wlanuieditprofile**</span><span class="sxs-lookup"><span data-stu-id="5592c-127">**WlanUIEditProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
