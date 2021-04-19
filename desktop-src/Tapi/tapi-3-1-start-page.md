---
description: Die Microsoft Telefonie-Version 3,1 ist Component Object Model eine COM-basierte API, die klassische und IP-Telefonie zusammenfasst.
ms.assetid: 79c4d2c9-953e-4e68-98b7-6a0dd9a04e0b
title: Telefonie-Anwendungsprogrammierschnittstelle Version 3,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d302f6ffe67094d436caf94cc8cf109e1e3c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362383"
---
# <a name="telephony-application-programming-interface-version-31"></a><span data-ttu-id="89d96-103">Telefonie-Anwendungsprogrammierschnittstelle Version 3,1</span><span class="sxs-lookup"><span data-stu-id="89d96-103">Telephony Application Programming Interface Version 3.1</span></span>

## <a name="purpose"></a><span data-ttu-id="89d96-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="89d96-104">Purpose</span></span>

<span data-ttu-id="89d96-105">Die Microsoft Telefonie-Version 3,1 ist Component Object Model eine COM-basierte API, die klassische und IP-Telefonie zusammenfasst.</span><span class="sxs-lookup"><span data-stu-id="89d96-105">The Microsoft Telephony Application Programming Interface (TAPI) version 3.1 is a Component Object Model (COM)-based API that merges classic and IP telephony.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="89d96-106">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="89d96-106">Where applicable</span></span>

<span data-ttu-id="89d96-107">Mögliche TAPI-Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="89d96-107">Possible TAPI applications include:</span></span>

-   <span data-ttu-id="89d96-108">Multicast-Multimedia-IP-Konferenzen mit Dienst Qualität (Quality of Service, QoS)</span><span class="sxs-lookup"><span data-stu-id="89d96-108">Multicast multimedia IP conferencing with quality of service (QOS)</span></span>
-   <span data-ttu-id="89d96-109">Sprachanrufe über das Internet mithilfe des H. 323-Protokolls</span><span class="sxs-lookup"><span data-stu-id="89d96-109">Voice calls over the Internet using the H.323 protocol</span></span>
-   <span data-ttu-id="89d96-110">Callcenter-Anwendungen, die mehrere Agents nachverfolgen können</span><span class="sxs-lookup"><span data-stu-id="89d96-110">Call center applications capable of tracking multiple agents</span></span>
-   <span data-ttu-id="89d96-111">Einfache Sprachanrufe im Public-Switched-Telefon Netzwerk (PSTN)</span><span class="sxs-lookup"><span data-stu-id="89d96-111">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="89d96-112">PBX-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="89d96-112">PBX control</span></span>
-   <span data-ttu-id="89d96-113">Interaktive sprach antwortsysteme (IVR)</span><span class="sxs-lookup"><span data-stu-id="89d96-113">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="89d96-114">Voicemail</span><span class="sxs-lookup"><span data-stu-id="89d96-114">Voice mail</span></span>

## <a name="developer-audience"></a><span data-ttu-id="89d96-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="89d96-115">Developer audience</span></span>

<span data-ttu-id="89d96-116">Sie können TAPI-fähige Anwendungen in vielen Sprachen schreiben, einschließlich Java, Visual Basic und C/C++.</span><span class="sxs-lookup"><span data-stu-id="89d96-116">You can write TAPI-enabled applications in many languages, including Java, Visual Basic, and C/C++.</span></span> <span data-ttu-id="89d96-117">Vertrautheit mit com ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89d96-117">Familiarity with COM is required.</span></span> <span data-ttu-id="89d96-118">Das Entwicklungsverfahren mit Telekommunikations-oder anderen Telefonieanwendungen ist hilfreich, aber nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="89d96-118">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="89d96-119">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="89d96-119">Run-time requirements</span></span>

<span data-ttu-id="89d96-120">TAPI Version 3,1 ermöglicht die Entwicklung von Kommunikationsanwendungen für Windows Server 2003-Betriebssysteme, Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="89d96-120">TAPI version 3.1 enables development of communications applications for Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="89d96-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="89d96-121">In this section</span></span>



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="89d96-122">Thema</span><span class="sxs-lookup"><span data-stu-id="89d96-122">Topic</span></span></th><th><span data-ttu-id="89d96-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89d96-123">Description</span></span></th></tr></thead><tbody><tr class="odd"><td><span data-ttu-id="89d96-124"><a href="tapi-3-1-overview.md">Übersicht</a></span><span class="sxs-lookup"><span data-stu-id="89d96-124"><a href="tapi-3-1-overview.md">Overview</a></span></span><br/></td><td><span data-ttu-id="89d96-125">Allgemeine Informationen über die TAPI-Architektur und-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="89d96-125">General information about TAPI architecture and components.</span></span><br/></td></tr><tr class="even"><td><span data-ttu-id="89d96-126">Referenz</span><span class="sxs-lookup"><span data-stu-id="89d96-126">Reference</span></span><br/></td><td><span data-ttu-id="89d96-127">Dokumentation zu:</span><span class="sxs-lookup"><span data-stu-id="89d96-127">Documentation for:</span></span><br/><ul><li><span data-ttu-id="89d96-128"><a href="call-and-media-controls-reference.md">Verweise auf Aufrufe und mediensteuer Elemente</a></span><span class="sxs-lookup"><span data-stu-id="89d96-128"><a href="call-and-media-controls-reference.md">Call and Media Controls Reference</a></span></span></li><li><span data-ttu-id="89d96-129"><a href="call-center-controls-reference.md">Referenz für Callcenter-Steuerelemente</a></span><span class="sxs-lookup"><span data-stu-id="89d96-129"><a href="call-center-controls-reference.md">Call Center Controls Reference</a></span></span></li><li><span data-ttu-id="89d96-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous-Referenz</a></span><span class="sxs-lookup"><span data-stu-id="89d96-130"><a href="rendezvous-ip-telephony-conferencing-reference.md">Rendezvous Reference</a></span></span></li></ul></td></tr></tbody></table>



 

## <a name="related-topics"></a><span data-ttu-id="89d96-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89d96-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d96-132">Übersicht über Microsoft-Telefonie</span><span class="sxs-lookup"><span data-stu-id="89d96-132">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="89d96-133">TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="89d96-133">TAPI 2.2</span></span>](./tapi-2-2-start-page.md)
</dt> <dt>

[<span data-ttu-id="89d96-134">TAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="89d96-134">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

