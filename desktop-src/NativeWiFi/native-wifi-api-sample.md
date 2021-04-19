---
description: Veranschaulicht die Verwendung grundlegender drahtloser Netzwerk Verwaltungsfunktionen.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Native WiFi-API-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349842"
---
# <a name="native-wifi-api-sample"></a><span data-ttu-id="b5e89-103">Native WiFi-API-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b5e89-103">Native Wifi API Sample</span></span>

<span data-ttu-id="b5e89-104">Ein System eigenes WiFi-API-Beispiel, das die Verwendung grundlegender Drahtlos Netzwerk-Verwaltungsfunktionen veranschaulicht, ist im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="b5e89-104">A Native Wifi API sample that demonstrates the use of basic wireless network management functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b5e89-105">Die neueste Version der Windows SDK ist im [Download Center](https://developer.microsoft.com/windows/downloads)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b5e89-105">The latest version of the Windows SDK is available from the [Download Center](https://developer.microsoft.com/windows/downloads).</span></span>

<span data-ttu-id="b5e89-106">Standardmäßig wird der Native WiFi-Beispiel Quellcode im folgenden Verzeichnis installiert:</span><span class="sxs-lookup"><span data-stu-id="b5e89-106">By default, the Native Wifi sample source code is installed in the following directory:</span></span>

<span data-ttu-id="b5e89-107">**C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ <version number> \\ Samples \\ netds \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="b5e89-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="b5e89-108">Das Native WiFi-API-Beispiel befindet sich im folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="b5e89-108">The Native Wifi API sample is located under the following folder:</span></span>

<span data-ttu-id="b5e89-109">**autoConfig**</span><span class="sxs-lookup"><span data-stu-id="b5e89-109">**autoconfig**</span></span>

<span data-ttu-id="b5e89-110">Das Native WiFi-Beispiel kann unter Windows Vista und höher, Windows XP mit Service Pack 3 (SP3) und Wireless LAN API für Windows XP mit Service Pack 2 (SP2) kompiliert und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b5e89-110">The Native Wifi sample can be compiled and run on Windows Vista and later, Windows XP with Service Pack 3 (SP3), and Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="b5e89-111">Einige Features des Beispiels werden unter Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5e89-111">Some features of the sample are not supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="b5e89-112">Eine Liste der Funktionen, die von Windows XP mit SP3 und der Wireless LAN-API für Windows XP mit SP2 unterstützt werden, finden Sie [unter Native WiFi-API-Unterstützung unter Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span><span class="sxs-lookup"><span data-stu-id="b5e89-112">For a list of functions supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, see [Native Wifi API Support on Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span></span>

<span data-ttu-id="b5e89-113">Das Native WiFi-Beispiel veranschaulicht, wie die folgenden Aufgaben ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="b5e89-113">The Native Wifi sample demonstrates how to perform the following tasks:</span></span>

-   <span data-ttu-id="b5e89-114">Listet drahtlose Schnittstellen auf.</span><span class="sxs-lookup"><span data-stu-id="b5e89-114">Enumerate wireless interfaces.</span></span> <span data-ttu-id="b5e89-115">Weitere Informationen finden Sie unter [**wlanenuminterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span><span class="sxs-lookup"><span data-stu-id="b5e89-115">See [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span></span>
-   <span data-ttu-id="b5e89-116">Nutzen Sie die Funktionen einer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5e89-116">Get the capabilities of an interface.</span></span> <span data-ttu-id="b5e89-117">Weitere Informationen finden Sie unter [**wlangetinterfakecapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span><span class="sxs-lookup"><span data-stu-id="b5e89-117">See [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span></span>

    <span data-ttu-id="b5e89-118">\* \* Windows XP mit SP3 und Wireless LAN API für Windows XP mit SP2: \* \* Diese Funktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5e89-118">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* This feature is not supported.</span></span>

-   <span data-ttu-id="b5e89-119">Abfragen einer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5e89-119">Query an interface.</span></span> <span data-ttu-id="b5e89-120">Weitere Informationen finden Sie unter [**wlanqueryinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span><span class="sxs-lookup"><span data-stu-id="b5e89-120">See [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span></span>
-   <span data-ttu-id="b5e89-121">Festlegen von Parametern für eine Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5e89-121">Set parameters for a network interface.</span></span> <span data-ttu-id="b5e89-122">Weitere Informationen finden Sie unter [**wlansetinterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span><span class="sxs-lookup"><span data-stu-id="b5e89-122">See [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span></span> <span data-ttu-id="b5e89-123">Diese Funktion kann verwendet werden, um das drahtlose Radio zu aktivieren und zu deaktivieren (und damit Drahtlos Netzwerk Konnektivität zu aktivieren oder zu deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="b5e89-123">This function can be used to turn the wireless radio on and off (and therefore enable or disable wireless network connectivity).</span></span>
-   <span data-ttu-id="b5e89-124">Suchen Sie nach verfügbaren Drahtlos Netzwerken.</span><span class="sxs-lookup"><span data-stu-id="b5e89-124">Scan for available wireless networks.</span></span> <span data-ttu-id="b5e89-125">Siehe [**wlanscan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span><span class="sxs-lookup"><span data-stu-id="b5e89-125">See [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span></span>
-   <span data-ttu-id="b5e89-126">Hier finden Sie eine Liste der verfügbaren oder sichtbaren Drahtlos Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="b5e89-126">Get the list of available or visible wireless networks.</span></span> <span data-ttu-id="b5e89-127">Weitere Informationen finden Sie unter [**wlangetavailablenetworklist**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span><span class="sxs-lookup"><span data-stu-id="b5e89-127">See [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span></span>
-   <span data-ttu-id="b5e89-128">Hiermit können Sie ein Profil erstellen, speichern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="b5e89-128">Get, save, or delete a profile.</span></span> <span data-ttu-id="b5e89-129">Weitere Informationen finden Sie unter [**wlangetprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)und [**wlandeleteprofile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span><span class="sxs-lookup"><span data-stu-id="b5e89-129">See [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), and [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span></span>
-   <span data-ttu-id="b5e89-130">Herstellen einer Verbindung mit einem Drahtlos Netzwerk oder Trennen der Verbindung.</span><span class="sxs-lookup"><span data-stu-id="b5e89-130">Connect to or disconnect from a wireless network.</span></span> <span data-ttu-id="b5e89-131">Weitere Informationen finden Sie unter [**wlanconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) und [**wlandisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span><span class="sxs-lookup"><span data-stu-id="b5e89-131">See [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5e89-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5e89-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5e89-133">Verwenden von nativem WiFi</span><span class="sxs-lookup"><span data-stu-id="b5e89-133">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="b5e89-134">Windows Vista-drahtlos-SDK-Forum</span><span class="sxs-lookup"><span data-stu-id="b5e89-134">Windows Vista Wireless SDK Forum</span></span>](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

<span data-ttu-id="b5e89-135">[Problembehandlung bei drahtlosen Windows Vista 802,11-Verbindungen](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="b5e89-135">[Troubleshooting Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span></span>
</dt> </dl>

 

 
