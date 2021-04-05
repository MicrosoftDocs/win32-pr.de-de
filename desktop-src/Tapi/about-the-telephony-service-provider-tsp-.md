---
description: Ein TAPI-Telefoniedienstanbieter (DSP) ist eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: Informationen zum Telefoniedienstanbieter (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750792"
---
# <a name="about-the-telephony-service-provider-tsp"></a><span data-ttu-id="1dbe1-103">Informationen zum Telefoniedienstanbieter (TSP)</span><span class="sxs-lookup"><span data-stu-id="1dbe1-103">About the Telephony Service Provider (TSP)</span></span>

<span data-ttu-id="1dbe1-104">\[ Die TSPS h323 und ipconf sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1dbe1-104">\[ The H323 and IPConf TSPs are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1dbe1-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1dbe1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1dbe1-106">Ein TAPI-Telefoniedienstanbieter (DSP) ist eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1dbe1-106">A TAPI telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="1dbe1-107">Eine TAPI-Anwendung verwendet standardisierte Befehle, TAPI übergibt die Bildung an den Telefoniedienstanbieter, und der TSP verarbeitet die spezifischen Befehle, die mit dem Gerät ausgetauscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1dbe1-107">A TAPI application uses standardized commands, TAPI passes in formation to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="1dbe1-108">In den folgenden Abschnitten werden die in Microsoft Windows bereitgestellten TSPS kurz beschrieben:</span><span class="sxs-lookup"><span data-stu-id="1dbe1-108">The following sections briefly describe the TSPs provided with Microsoft Windows:</span></span>

-   [<span data-ttu-id="1dbe1-109">H323-TSP</span><span class="sxs-lookup"><span data-stu-id="1dbe1-109">H323 TSP</span></span>](h323-tsp.md)
-   [<span data-ttu-id="1dbe1-110">Ipconf-TSP</span><span class="sxs-lookup"><span data-stu-id="1dbe1-110">IPConf TSP</span></span>](ipconf-tsp.md)
-   [<span data-ttu-id="1dbe1-111">Gerätetreiber-TSP im Kernelmodus</span><span class="sxs-lookup"><span data-stu-id="1dbe1-111">Kernel-Mode Device Driver TSP</span></span>](kernel-mode-device-driver-tsp.md)
-   [<span data-ttu-id="1dbe1-112">NDIS-Proxy-TSP</span><span class="sxs-lookup"><span data-stu-id="1dbe1-112">NDIS Proxy TSP</span></span>](ndis-proxy-tsp.md)
-   [<span data-ttu-id="1dbe1-113">Remote-TSP</span><span class="sxs-lookup"><span data-stu-id="1dbe1-113">Remote TSP</span></span>](remote-tsp.md)
-   [<span data-ttu-id="1dbe1-114">TSP von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="1dbe1-114">Third-Party TSP</span></span>](third-party-tsp.md)
-   [<span data-ttu-id="1dbe1-115">Unimodem-TSP</span><span class="sxs-lookup"><span data-stu-id="1dbe1-115">Unimodem TSP</span></span>](unimodem-tsp.md)

<span data-ttu-id="1dbe1-116">Ausführliche Informationen finden Sie im Ressourcenkit für das Ziel Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="1dbe1-116">For detailed information, please see the Resource Kit for the target operating system.</span></span> <span data-ttu-id="1dbe1-117">TSPS von Drittanbietern für spezialisierte Kommunikationsgeräte werden in der Regel vom Hersteller bereitgestellt und mit dem Gerät installiert.</span><span class="sxs-lookup"><span data-stu-id="1dbe1-117">Third-party TSPs for specialized communications devices will typically be provided by the manufacturer and will be installed with the device.</span></span>

<span data-ttu-id="1dbe1-118">In den folgenden Themen wird beschrieben, wie ein TSP erstellt wird, der in der Microsoft-Telefonieumgebung ordnungsgemäß funktioniert und wie ein TSP/MSP-paar erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="1dbe1-118">The following topics describe how to create a TSP that will function properly within the Microsoft Telephony environment, and how to create a TSP/MSP pair:</span></span>

-   [<span data-ttu-id="1dbe1-119">Telefoniedienstanbieter-Schnittstelle (TSPI)</span><span class="sxs-lookup"><span data-stu-id="1dbe1-119">Telephony Service Provider Interface (TSPI)</span></span>](telephony-service-provider-interface-tspi-.md)
-   [<span data-ttu-id="1dbe1-120">TSPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1dbe1-120">TSPI Reference</span></span>](tspi-reference.md)
-   [<span data-ttu-id="1dbe1-121">Medien Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1dbe1-121">Media Service Providers</span></span>](./media-service-providers-start-page.md)

> [!Note]  
> <span data-ttu-id="1dbe1-122">Ein TSP ist eine vom Benutzer erstellte DLL.</span><span class="sxs-lookup"><span data-stu-id="1dbe1-122">A TSP is a user-created DLL.</span></span> <span data-ttu-id="1dbe1-123">Wenn Sie einen TSP für eine 64-Bit-Windows-Plattform erstellen, müssen Sie Sie als 64-Bit-DLL oder DLLs kompilieren.</span><span class="sxs-lookup"><span data-stu-id="1dbe1-123">If you are creating a TSP for a 64-bit Windows platform, you must compile it as a 64-bit DLL or DLLs.</span></span>

 

 

 
