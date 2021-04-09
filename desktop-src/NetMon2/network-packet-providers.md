---
description: Netzwerk Paketanbieter (NPPs) sind Netzwerkmonitor Systemkomponenten, die Netzwerk Datenverkehr (Frames) aus dem Netzwerk erfassen und an die Netzwerkmonitor-Benutzeroberfläche und NPP-Anwendungen weiterleiten.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Netzwerk Paketanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868824"
---
# <a name="network-packet-providers"></a><span data-ttu-id="1bf5a-103">Netzwerk Paketanbieter</span><span class="sxs-lookup"><span data-stu-id="1bf5a-103">Network Packet Providers</span></span>

<span data-ttu-id="1bf5a-104">Netzwerk Paketanbieter (NPPs) sind Netzwerkmonitor Systemkomponenten, die Netzwerk Datenverkehr (Frames) aus dem Netzwerk erfassen und an die Netzwerkmonitor-Benutzeroberfläche und [*NPP-Anwendungen*](n.md)weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-104">Network packet providers (NPPs) are Network Monitor system components that collect network traffic (frames) from the network and pass them on to the Network Monitor UI, and [*NPP applications*](n.md).</span></span>

<span data-ttu-id="1bf5a-105">Die folgende Abbildung zeigt zwei NPPs: das von Netzwerkmonitor bereitgestellte NDIS NPP und ein benutzerdefiniertes NPP.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-105">The following illustration shows two NPPs: the NDIS NPP provided by Network Monitor and a custom NPP.</span></span>

![NDIS NPP von Netzwerkmonitor und benutzerdefiniertem NPP bereitgestellt](images/npp.png)

<span data-ttu-id="1bf5a-107">Der von Netzwerkmonitor bereitgestellte NDIS-npp ist Ndisnpp.dll.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-107">The NDIS NPP provided by Network Monitor is Ndisnpp.dll.</span></span> <span data-ttu-id="1bf5a-108">Dieser NPP verwendet den Netzwerkmonitor System Treiber (Nmnt.sys), um die vom Netzwerk gesammelten Frames und verschiedene COM-Schnittstellen (als NPP-Schnittstellen bezeichnet) zu erhalten, um die Frames an die Netzwerkmonitor-Benutzeroberfläche und NPP-Anwendungen zu übergeben, in denen Sie angezeigt und analysiert werden können.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-108">This NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network and several COM interfaces (referred to as the NPP interfaces) to pass the frames on to the Network Monitor UI, and NPP applications, where they can be displayed and analyzed.</span></span>

<span data-ttu-id="1bf5a-109">Ndisnpp.dll stellt eine Verbindung mit der [*NDIS*](n.md) -Schicht her, um den Netzwerk Datenverkehr abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-109">Ndisnpp.dll connects to the [*NDIS*](n.md) layer to obtain its network traffic.</span></span> <span data-ttu-id="1bf5a-110">(Benutzerdefinierte NPPs können die NDIS-Schicht umgehen und direkt mit der Netzwerkhardware kommunizieren.) Beachten Sie, dass NPPs unabhängig davon, ob NPP NDIS verwendet, eine Verbindung mit einer beliebigen Anzahl von Netzwerkkarten herstellen kann und dass alle NPPs die gleichen NPP-Schnittstellen unterstützen müssen.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-110">(Custom NPPs can bypass the NDIS layer and communicate directly with the networking hardware.) Be aware that regardless of whether an NPP uses NDIS, NPPs can connect to any number of network cards and that all NPPs must support the same NPP interfaces.</span></span>

<span data-ttu-id="1bf5a-111">Bevor eine Anwendung mit dem Erfassen von Daten beginnen kann, müssen Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="1bf5a-111">Before an application can start to capture data, it must:</span></span>

-   <span data-ttu-id="1bf5a-112">Wählen Sie die Netzwerkschnittstellenkarte (NIC) aus, mit der der NPP mit dem Netzwerk verbunden wird.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-112">Select the network interface card (NIC) that will connect the NPP to the network.</span></span>
-   <span data-ttu-id="1bf5a-113">Wählen Sie die NPP-Schnittstelle aus, die zum Erfassen der Netzwerk Rahmen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-113">Select the NPP interface that will be used to capture the network frames.</span></span>
-   <span data-ttu-id="1bf5a-114">Verwenden Sie die ausgewählte Schnittstelle, um eine Verbindung mit der NIC herzustellen.</span><span class="sxs-lookup"><span data-stu-id="1bf5a-114">Use the selected interface to connect to the NIC.</span></span>

<span data-ttu-id="1bf5a-115">Weitere Informationen zum Auflisten und Auswählen einer Netzwerkschnittstellenkarte finden Sie unter [Auswählen einer Netzwerkschnittstellenkarte](selecting-a-network-interface-card.md).</span><span class="sxs-lookup"><span data-stu-id="1bf5a-115">For more information about how to enumerate and select a network interface card, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md).</span></span>

<span data-ttu-id="1bf5a-116">Weitere Informationen zu von NPPs verfügbar gemachten com-Schnittstellen finden Sie unter [Auswählen einer NPP-Schnittstelle](selecting-an-npp-interface.md).</span><span class="sxs-lookup"><span data-stu-id="1bf5a-116">For more information about COM interfaces exposed by NPPs, see [Selecting an NPP Interface](selecting-an-npp-interface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bf5a-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bf5a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bf5a-118">**Idelta-DC**</span><span class="sxs-lookup"><span data-stu-id="1bf5a-118">**IDelaydC**</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="1bf5a-119">**IESP**</span><span class="sxs-lookup"><span data-stu-id="1bf5a-119">**IESP**</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="1bf5a-120">**"Iran"**</span><span class="sxs-lookup"><span data-stu-id="1bf5a-120">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="1bf5a-121">**IStats**</span><span class="sxs-lookup"><span data-stu-id="1bf5a-121">**IStats**</span></span>](istats.md)
</dt> </dl>

 

 



