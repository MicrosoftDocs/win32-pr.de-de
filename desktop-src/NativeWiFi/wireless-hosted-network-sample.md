---
description: Veranschaulicht die Verwendung von drahtlos gehosteten Netzwerkfunktionen.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Beispiel für drahtlos gehostete Netzwerke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368113"
---
# <a name="wireless-hosted-network-sample"></a><span data-ttu-id="2c5e0-103">Beispiel für drahtlos gehostete Netzwerke</span><span class="sxs-lookup"><span data-stu-id="2c5e0-103">Wireless Hosted Network Sample</span></span>

<span data-ttu-id="2c5e0-104">Ein Beispiel für ein drahtlos gehostetes Netzwerk, das die Verwendung von drahtlosen gehosteten Netzwerkfunktionen veranschaulicht, ist im Microsoft Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-104">A wireless Hosted Network sample that demonstrates the use of wireless Hosted Network functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2c5e0-105">Die neueste Version der Windows SDK ist im [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-105">The latest version of the Windows SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span>

<span data-ttu-id="2c5e0-106">Standardmäßig ist der Quell Code des drahtlos gehosteten Netzwerks im folgenden Verzeichnis installiert:</span><span class="sxs-lookup"><span data-stu-id="2c5e0-106">By default, the wireless Hosted Network sample source code is installed in the following directory:</span></span>

<span data-ttu-id="2c5e0-107">**C: \\ Programmdateien \\ Microsoft sdert \\ Windows \\ v 7.0 \\ Beispiele \\ netds \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="2c5e0-108">Das Beispiel für drahtlos gehostete Netzwerke befindet sich im folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="2c5e0-108">The wireless Hosted Network sample is located under the following folder:</span></span>

<span data-ttu-id="2c5e0-109">**Wirelesshostednetwork**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-109">**WirelessHostedNetwork**</span></span>

<span data-ttu-id="2c5e0-110">Das Beispiel für drahtlos gehostete Netzwerke kann auf der Windows SDK für Windows 7 kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-110">The Wireless Hosted Network sample can be compiled on the Windows SDK for Windows 7.</span></span> <span data-ttu-id="2c5e0-111">Das Beispiel für drahtlos gehostete Netzwerke kann unter Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-111">The Wireless Hosted Network sample can be run on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span>

<span data-ttu-id="2c5e0-112">Unter Windows 7 und Windows Server 2008 R2 mit installiertem drahtlosen LAN-Dienst wird vom Betriebssystem ein virtuelles Gerät installiert, wenn ein gehosteter netzwerkfähiger drahtloser Adapter auf dem Computer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-112">On Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine.</span></span> <span data-ttu-id="2c5e0-113">Dieses virtuelle Gerät wird normalerweise im Ordner "Netzwerkverbindungen" als "drahtlose Netzwerkverbindung 2" mit dem Gerätenamen "Microsoft Virtual WiFi Miniport Adapter" angezeigt, wenn der Computer über einen einzelnen drahtlosen Netzwerkadapter verfügt.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-113">This virtual device normally shows up in the "Network Connections Folder" as "Wireless Network Connection 2" with a Device Name of "Microsoft Virtual WiFi Miniport adapter" if the computer has a single wireless network adapter.</span></span> <span data-ttu-id="2c5e0-114">Dieses virtuelle Gerät wird ausschließlich zum Durchführen von Verbindungen mit Software Zugriffs Punkten (softap) verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-114">This virtual device is used exclusively for performing software access point (SoftAP) connections.</span></span> <span data-ttu-id="2c5e0-115">Die Lebensdauer dieses virtuellen Geräts ist an den physischen drahtlosen Adapter gebunden.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-115">The lifetime of this virtual device is tied to the physical wireless adapter.</span></span> <span data-ttu-id="2c5e0-116">Wenn der physische drahtlose Adapter deaktiviert ist, wird dieses virtuelle Gerät ebenfalls entfernt.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-116">If the physical wireless adapter is disabled, this virtual device will be removed as well.</span></span>

<span data-ttu-id="2c5e0-117">Die drahtlosen gehosteten Netzwerkfunktionen werden verwendet, um das drahtlos gehostete Netzwerk zu starten und zu unterbinden, Einstellungen zu konfigurieren oder zu ändern oder um Informationen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="2c5e0-117">The wireless Hosted Network functions are used to start and stop the wireless Hosted Network, configure or change settings, or query for information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c5e0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c5e0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c5e0-119">Informationen zum drahtlos gehosteten Netzwerk</span><span class="sxs-lookup"><span data-stu-id="2c5e0-119">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="2c5e0-120">Verwenden der Freigabe von gehosteten Netzwerken und Internet Verbindungen</span><span class="sxs-lookup"><span data-stu-id="2c5e0-120">Using Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[<span data-ttu-id="2c5e0-121">**Wlanhustednetworkforcestart**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-121">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[<span data-ttu-id="2c5e0-122">**Wlanhustednetworkinitsettings**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-122">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[<span data-ttu-id="2c5e0-123">**Wlanhustednetworkqueryproperty**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-123">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[<span data-ttu-id="2c5e0-124">**Wlanhustednetworkquerysecondarykey**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-124">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[<span data-ttu-id="2c5e0-125">**Wlanhustednetworkquerystatus**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-125">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[<span data-ttu-id="2c5e0-126">**Wlanhustednetworkrefreshsecuritysettings**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-126">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[<span data-ttu-id="2c5e0-127">**Wlanhustednetworksetproperty**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-127">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[<span data-ttu-id="2c5e0-128">**Wlanhustednetworksetsecondarykey**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-128">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[<span data-ttu-id="2c5e0-129">**Wlanhustednetworkstartusing**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-129">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[<span data-ttu-id="2c5e0-130">**Wlanhustednetworkstopusing**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-130">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[<span data-ttu-id="2c5e0-131">**Wlanregistervirtualstationnotification**</span><span class="sxs-lookup"><span data-stu-id="2c5e0-131">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



