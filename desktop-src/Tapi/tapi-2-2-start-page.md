---
description: Die Microsoft Telefonie-Version 2,2 (Application Programming Interface, TAPI), Version (TAPI/C), ermöglicht die Implementierung von Kommunikationsanwendungen im Bereich von grundlegenden Modem Steuerelementen bis hin zu Callcenter mit mehreren Agents und Switches.
ms.assetid: 02bfe923-9915-439e-ac7c-a570416d054a
title: Telefonie-Anwendungsprogrammierschnittstelle Version 2,2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0dc158210350979105d765dc939f600f61d8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216330"
---
# <a name="telephony-application-programming-interface-version-22"></a><span data-ttu-id="a67c2-103">Telefonie-Anwendungsprogrammierschnittstelle Version 2,2</span><span class="sxs-lookup"><span data-stu-id="a67c2-103">Telephony Application Programming Interface Version 2.2</span></span>

## <a name="purpose"></a><span data-ttu-id="a67c2-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="a67c2-104">Purpose</span></span>

<span data-ttu-id="a67c2-105">Die Microsoft Telefonie-Version 2,2 (Application Programming Interface, TAPI), Version (TAPI/C), ermöglicht die Implementierung von Kommunikationsanwendungen im Bereich von grundlegenden Modem Steuerelementen bis hin zu Callcenter mit mehreren Agents und Switches.</span><span class="sxs-lookup"><span data-stu-id="a67c2-105">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 (TAPI/C) enables implementation of communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a67c2-106">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="a67c2-106">Where applicable</span></span>

<span data-ttu-id="a67c2-107">Mögliche TAPI 2,2-Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="a67c2-107">Possible TAPI 2.2 applications include:</span></span>

-   <span data-ttu-id="a67c2-108">Einfache Sprachanrufe im Public-Switched-Telefon Netzwerk (PSTN)</span><span class="sxs-lookup"><span data-stu-id="a67c2-108">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="a67c2-109">Callcenter-Anwendungen zum Nachverfolgen mehrerer Agents</span><span class="sxs-lookup"><span data-stu-id="a67c2-109">Call center applications for tracking multiple agents</span></span>
-   <span data-ttu-id="a67c2-110">Modem Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a67c2-110">Modem control</span></span>
-   <span data-ttu-id="a67c2-111">PBX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a67c2-111">PBX control</span></span>
-   <span data-ttu-id="a67c2-112">Interaktive sprach antwortsysteme (IVR)</span><span class="sxs-lookup"><span data-stu-id="a67c2-112">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="a67c2-113">Voicemail</span><span class="sxs-lookup"><span data-stu-id="a67c2-113">Voice mail</span></span>
-   <span data-ttu-id="a67c2-114">Ausführliche Telefongeräte Steuerung</span><span class="sxs-lookup"><span data-stu-id="a67c2-114">Detailed phone device control</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a67c2-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="a67c2-115">Developer audience</span></span>

<span data-ttu-id="a67c2-116">TAPI/C ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="a67c2-116">TAPI/C is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="a67c2-117">Das Entwicklungsverfahren mit Telekommunikations-oder anderen Telefonieanwendungen ist hilfreich, aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a67c2-117">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a67c2-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="a67c2-118">Run-time requirements</span></span>

<span data-ttu-id="a67c2-119">TAPI Version 2,2 ermöglicht die Entwicklung von Kommunikationsanwendungen für die Betriebssysteme Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98 und Windows 95.</span><span class="sxs-lookup"><span data-stu-id="a67c2-119">TAPI version 2.2 enables development of communications applications for the Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, and Windows 95.</span></span> <span data-ttu-id="a67c2-120">Weitere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="a67c2-120">For more information about which operating systems support a particular function, see the Requirements section of the documentation for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a67c2-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a67c2-121">In this section</span></span>



| <span data-ttu-id="a67c2-122">Thema</span><span class="sxs-lookup"><span data-stu-id="a67c2-122">Topic</span></span>                                          | <span data-ttu-id="a67c2-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a67c2-123">Description</span></span>                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a67c2-124">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a67c2-124">Overview</span></span>](tapi-2-2-overview.md)<br/>   | <span data-ttu-id="a67c2-125">Allgemeine Informationen über die TAPI-Architektur und-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a67c2-125">General information about TAPI architecture and components.</span></span><br/>                                            |
| [<span data-ttu-id="a67c2-126">Verweis</span><span class="sxs-lookup"><span data-stu-id="a67c2-126">Reference</span></span>](tapi-2-2-reference.md)<br/> | <span data-ttu-id="a67c2-127">Dokumentation zu Funktionen, Strukturen, Meldungen, Konstanten und Geräteklassen, die in TAPI 2,2 verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a67c2-127">Documentation of functions, structures, messages, constants, and device classes available in TAPI 2.2.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a67c2-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a67c2-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a67c2-129">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="a67c2-129">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="a67c2-130">TAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a67c2-130">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

