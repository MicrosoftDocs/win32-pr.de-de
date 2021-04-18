---
description: Mit einem Medien Dienstanbieter (MSP) kann eine Anwendung Medien für einen bestimmten Transportmechanismus steuern.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Medien Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106371826"
---
# <a name="media-service-providers"></a><span data-ttu-id="9c5be-103">Medien Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9c5be-103">Media Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="9c5be-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="9c5be-104">Purpose</span></span>

<span data-ttu-id="9c5be-105">Mit einem Medien Dienstanbieter (MSP) kann eine Anwendung Medien für einen bestimmten Transportmechanismus steuern.</span><span class="sxs-lookup"><span data-stu-id="9c5be-105">A media service provider (MSP) enables an application to control media for a particular transport mechanism.</span></span> <span data-ttu-id="9c5be-106">Ein MSP wird immer einem Telefoniedienstanbieter (TSP) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9c5be-106">An MSP is always paired with a Telephony Service Provider (TSP).</span></span>

<span data-ttu-id="9c5be-107">Bei der Media Service Provider Interface (MSPi) handelt es sich um einen Satz von Schnittstellen und Methoden, die von einem MSP implementiert werden, um eine Anwendungssteuerung des Medien Transports während einer Kommunikationssitzung zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="9c5be-107">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow an application control over media transport during a communications session.</span></span> <span data-ttu-id="9c5be-108">Ein MSP verarbeitet die gerätespezifischen und Protokoll spezifischen Mechanismen, die erforderlich sind, um diese Steuerelemente zu implementieren, und kommuniziert mit dem gekoppelten TSP oder einer Anwendung durch die Verwendung der Methoden, die in der MSPi bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c5be-108">An MSP handles the device-specific and protocol-specific mechanisms required to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9c5be-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="9c5be-109">Developer audience</span></span>

<span data-ttu-id="9c5be-110">Vertrautheit mit com ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c5be-110">Familiarity with COM is required.</span></span> <span data-ttu-id="9c5be-111">Das Entwicklungsverfahren mit Telekommunikations-oder anderen Telefonieanwendungen ist hilfreich, aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c5be-111">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9c5be-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="9c5be-112">Run-time requirements</span></span>

<span data-ttu-id="9c5be-113">MSPi ermöglicht die Entwicklung von Medien Dienstanbietern für bestimmte Protokolle oder Geräte, die unter den Betriebssystemen Windows Server 2003, Windows XP und Windows 2000 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9c5be-113">MSPI enables development of media service providers for particular protocols or devices running on Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9c5be-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9c5be-114">In this section</span></span>



| <span data-ttu-id="9c5be-115">Thema</span><span class="sxs-lookup"><span data-stu-id="9c5be-115">Topic</span></span>                                                                       | <span data-ttu-id="9c5be-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9c5be-116">Description</span></span>                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="9c5be-117">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9c5be-117">Overview</span></span>](about-the-media-service-provider-msp-.md)<br/>            | <span data-ttu-id="9c5be-118">Allgemeine Informationen zur MSP-Architektur und-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9c5be-118">General information about MSP architecture and components.</span></span><br/> |
| [<span data-ttu-id="9c5be-119">Verweis</span><span class="sxs-lookup"><span data-stu-id="9c5be-119">Reference</span></span>](media-service-provider-interface-mspi-reference.md)<br/> | <span data-ttu-id="9c5be-120">Dokumentation für die MSPi-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="9c5be-120">Documentation for the MSPI interfaces.</span></span><br/>                     |



 

## <a name="related-topics"></a><span data-ttu-id="9c5be-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c5be-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c5be-122">Übersicht über Microsoft-Telefonie</span><span class="sxs-lookup"><span data-stu-id="9c5be-122">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="9c5be-123">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="9c5be-123">TAPI 3.1</span></span>](tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="9c5be-124">Telefoniedienstanbieter</span><span class="sxs-lookup"><span data-stu-id="9c5be-124">Telephony Service Providers</span></span>](./telephony-service-providers-start-page.md)
</dt> </dl>

 

