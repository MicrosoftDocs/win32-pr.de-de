---
description: Die Web Services on Devices-API (WSDAPI) bietet Unterstützung für das Geräte Profil für Webdienste (DPWS) unter Windows Vista, das die Kommunikation zwischen Windows-basierten PCs und Netzwerkgeräten ermöglicht.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: WSDAPI-Spezifikation Konformität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216154"
---
# <a name="wsdapi-specification-compliance"></a><span data-ttu-id="164b5-103">WSDAPI-Spezifikation Konformität</span><span class="sxs-lookup"><span data-stu-id="164b5-103">WSDAPI Specification Compliance</span></span>

<span data-ttu-id="164b5-104">Die Web Services on Devices-API (WSDAPI) bietet Unterstützung für das [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) unter Windows Vista, das die Kommunikation zwischen Windows-basierten PCs und Netzwerkgeräten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="164b5-104">Web Services on Devices API (WSDAPI) provides support for the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) on Windows Vista, which enables Web Services (WS) communication between Windows-based PCs and network connected devices.</span></span> <span data-ttu-id="164b5-105">DPWS assembliert grundlegende WS-Spezifikationen wie [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)und [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/)und erweitert oder beschränkt Sie, um einen grundlegenden Satz von Funktionen für Ressourcen eingeschränkte Geräte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="164b5-105">DPWS assembles basic WS specifications, such as [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf), and [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), and enhances or constrains them to provide a baseline set of capabilities for resource-constrained devices.</span></span> <span data-ttu-id="164b5-106">Diese grundlegende Spezifikation enthält erforderliche Funktionen, wie z. b. die Möglichkeit, die Eigenschaften des Geräts durch Metadaten zu beschreiben, und optionale Funktionen, wie z. b. die Möglichkeit, bestimmte Nachrichten aus Sicherheitsgründen abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="164b5-106">This baseline specification contains required functionality, such as the ability to describe properties of the device through metadata, and optional functionality, such as the ability to reject specific messages for security reasons.</span></span>

<span data-ttu-id="164b5-107">Die WSDAPI-Implementierung in Windows Vista ist die erste Version der expliziten Unterstützung für die DPWS und eine nicht verwaltete DPWS-Implementierung, die von anderen Webdienst Implementierungen (z. b. [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) oder [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)) getrennt und unterschiedlich ist.</span><span class="sxs-lookup"><span data-stu-id="164b5-107">The WSDAPI implementation in Windows Vista is the first release of explicit support for the DPWS, and is an unmanaged implementation of DPWS that is separate and distinct from other Web Services implementations (such as the [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) or [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)).</span></span>

<span data-ttu-id="164b5-108">Die folgenden Themen sind für Gerätehersteller und andere geräteimplementierer von Interesse, die Geräte erstellen, die mit Windows-basierten WSDAPI-Clients und-Hosts interagieren, ohne WSDAPI zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="164b5-108">The following topics are of interest to device manufacturers and other device implementers that create devices that interoperate with Windows-based WSDAPI clients and hosts without using WSDAPI.</span></span> <span data-ttu-id="164b5-109">In diesen Themen wird die Implementierung von WSDAPI in Bezug auf die zugrunde liegenden Spezifikationen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="164b5-109">These topics describe the implementation of WSDAPI relative to the underlying specifications.</span></span> <span data-ttu-id="164b5-110">Sie umfassen die Implementierung von erforderlichen Funktionen, optionalen Funktionen und zusätzlichen Funktionen, die nicht in der Spezifikation definiert sind.</span><span class="sxs-lookup"><span data-stu-id="164b5-110">They cover the implementation of required functionality, optional functionality, and additional functionality not defined in the specification.</span></span>

-   [<span data-ttu-id="164b5-111">Konformität der DPWS-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="164b5-111">DPWS Specification Compliance</span></span>](dpws-specification-compliance.md)
-   [<span data-ttu-id="164b5-112">Konformität der WS-Discovery-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="164b5-112">WS-Discovery Specification Compliance</span></span>](ws-discovery-specification-compliance.md)
-   [<span data-ttu-id="164b5-113">Konformität mit WS-MetadataExchange und WS-Transfer Spezifikation</span><span class="sxs-lookup"><span data-stu-id="164b5-113">WS-MetadataExchange and WS-Transfer Specification Compliance</span></span>](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [<span data-ttu-id="164b5-114">Zusätzliche WS-Discovery Funktionen</span><span class="sxs-lookup"><span data-stu-id="164b5-114">Additional WS-Discovery Functionality</span></span>](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a><span data-ttu-id="164b5-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="164b5-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="164b5-116">WSD-Geräteentwicklung</span><span class="sxs-lookup"><span data-stu-id="164b5-116">WSD Device Development</span></span>](wsd-device-development.md)
</dt> <dt>

[<span data-ttu-id="164b5-117">Empfehlungen zur Implementierung der WSD-Geräte</span><span class="sxs-lookup"><span data-stu-id="164b5-117">WSD Device Implementation Recommendations</span></span>](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
