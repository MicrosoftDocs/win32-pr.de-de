---
description: Bei einem Telefoniedienstanbieter (TSP) handelt es sich um eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt.
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: Telefoniedienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868144"
---
# <a name="telephony-service-providers"></a><span data-ttu-id="d4a39-103">Telefoniedienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d4a39-103">Telephony Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="d4a39-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="d4a39-104">Purpose</span></span>

<span data-ttu-id="d4a39-105">Bei einem Telefoniedienstanbieter (TSP) handelt es sich um eine Dynamic Link Library (dll), die die Kommunikation von Geräten über einen Satz exportierter Dienstfunktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4a39-105">A telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="d4a39-106">Eine TAPI-Anwendung verwendet standardisierte Befehle, TAPI übergibt Informationen an den Telefoniedienstanbieter, und der TSP verarbeitet die spezifischen Befehle, die mit dem Gerät ausgetauscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d4a39-106">A TAPI application uses standardized commands, TAPI passes information to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="d4a39-107">Ein TSP muss der Telefoniedienstanbieter-Schnittstelle (TSPI) entsprechen, um in der Microsoft-Telefonieumgebung als Dienstanbieter zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="d4a39-107">A TSP must conform to the Telephony Service Provider Interface (TSPI) to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="d4a39-108">TSPI definiert die externen Funktionen, die von einem Telefoniedienstanbieter zur Verfügung gestellt werden</span><span class="sxs-lookup"><span data-stu-id="d4a39-108">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d4a39-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="d4a39-109">Developer audience</span></span>

<span data-ttu-id="d4a39-110">Sie können TAPI-fähige Anwendungen in vielen Sprachen schreiben, einschließlich Java, Visual Basic und C/C++.</span><span class="sxs-lookup"><span data-stu-id="d4a39-110">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="d4a39-111">Vorherige Entwicklungsarbeiten mit Telekommunikations-oder anderen Telefonieanwendungen sind hilfreich, aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4a39-111">Previous development experience with telecommunications or other telephony applications is helpful but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d4a39-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="d4a39-112">Run-time requirements</span></span>

<span data-ttu-id="d4a39-113">TSPI ermöglicht die Entwicklung von TSPS für alle Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="d4a39-113">TSPI enables development of TSPs for all versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4a39-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d4a39-114">In this section</span></span>



| <span data-ttu-id="d4a39-115">Thema</span><span class="sxs-lookup"><span data-stu-id="d4a39-115">Topic</span></span>                                                                | <span data-ttu-id="d4a39-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4a39-116">Description</span></span>                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="d4a39-117">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d4a39-117">Overview</span></span>](about-the-telephony-service-provider-tsp-.md)<br/> | <span data-ttu-id="d4a39-118">Allgemeine Informationen über die Architektur und Komponenten von TSPI.</span><span class="sxs-lookup"><span data-stu-id="d4a39-118">General information about TSPI's architecture and components.</span></span><br/> |
| [<span data-ttu-id="d4a39-119">Verweis</span><span class="sxs-lookup"><span data-stu-id="d4a39-119">Reference</span></span>](tspi-reference.md)<br/>                           | <span data-ttu-id="d4a39-120">Dokumentation für die TSPI-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="d4a39-120">Documentation for the TSPI interfaces.</span></span><br/>                        |



 

## <a name="related-topics"></a><span data-ttu-id="d4a39-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d4a39-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4a39-122">Übersicht über Microsoft-Telefonie</span><span class="sxs-lookup"><span data-stu-id="d4a39-122">Microsoft Telephony Overview</span></span>](./microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="d4a39-123">Medien Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d4a39-123">Media Service Providers</span></span>](./media-service-providers-start-page.md)
</dt> <dt>

[<span data-ttu-id="d4a39-124">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="d4a39-124">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="d4a39-125">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="d4a39-125">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> </dl>

 

