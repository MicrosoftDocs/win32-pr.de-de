---
description: TAPI 3-und mediensteuer Elemente sind ein generischer Satz von COM-Objekten, Schnittstellen und Methoden zum Aufrufen von zwei oder mehr Computern.
ms.assetid: e345df2f-1b68-41be-ac2d-b771136ee831
title: Informationen zu den Steuerelementen "Callcenter"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65d1a10d004cb16e0ba8753c27665cb7a30ff3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869564"
---
# <a name="about-call-and-media-controls"></a><span data-ttu-id="daa54-103">Informationen zu den Steuerelementen "Callcenter"</span><span class="sxs-lookup"><span data-stu-id="daa54-103">About Call And Media Controls</span></span>

<span data-ttu-id="daa54-104">TAPI 3-und mediensteuer Elemente sind ein generischer Satz von COM-Objekten, Schnittstellen und Methoden zum Aufrufen von zwei oder mehr Computern.</span><span class="sxs-lookup"><span data-stu-id="daa54-104">TAPI 3 call and media controls are a generic set of COM objects, interfaces, and methods for making calls between two or more machines.</span></span> <span data-ttu-id="daa54-105">Im Zusammenhang mit TAPI 3 bezieht sich der *Anruf* nicht nur auf die Sprachübertragung über das Public-Switched-Telefon Netzwerk (PSTN), sondern auf alle Mittel-und Transportmechanismen, für die Dienstanbieter vorhanden sind, z. b. eine Multicast Konferenz für Multimedia, die auf einem Unternehmens Intranet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="daa54-105">In the context of TAPI 3, *call* refers not just to voice transmission over the public switched telephone network (PSTN) but to any medium and transport mechanism for which service providers exist: for example, a multimedia multicast conference running on a corporate intranet.</span></span>

<span data-ttu-id="daa54-106">Die fünf Hauptobjekte im TAPI 3-Aufruf und die Medien Steuerungsarchitektur sind [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md) [,](call-object.md) [callhub und callhub](callhub-object.md).</span><span class="sxs-lookup"><span data-stu-id="daa54-106">The five main objects in the TAPI 3 call and media control architecture are [TAPI](tapi-object.md), [Address](address-object.md), [Terminal](terminal-object.md), [Call](call-object.md), and [CallHub](callhub-object.md).</span></span> <span data-ttu-id="daa54-107">Außerdem wurde Bereitstellung für [anbieterspezifische Schnittstellen](provider-specific-interfaces.md)vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="daa54-107">In addition, provision has been made for [provider-specific interfaces](provider-specific-interfaces.md).</span></span>

<span data-ttu-id="daa54-108">Im folgenden Diagramm wird veranschaulicht, wie diese Objekte interagieren.</span><span class="sxs-lookup"><span data-stu-id="daa54-108">The following diagram illustrates how these objects interact.</span></span>

![Interaktionen zwischen TAPI 3,0-anrufen und Medien steuerungsobjekten](images/sdkobj2.png)

## <a name="features"></a><span data-ttu-id="daa54-110">Features</span><span class="sxs-lookup"><span data-stu-id="daa54-110">Features</span></span>

-   <span data-ttu-id="daa54-111">Abstrahiert sowohl die Funktion zum Abrufen als auch der Medien, um unterschiedliche und scheinbar nicht kompatible Kommunikationsprotokolle zu ermöglichen und eine gemeinsame Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="daa54-111">Abstracts both call and media functionality to allow different and seemingly incompatible communication protocols to expose a common interface to applications.</span></span>
-   <span data-ttu-id="daa54-112">Basierend auf dem Component Object Model (com), sodass Anwendungen in nahezu jeder Sprache geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="daa54-112">Based on the Component Object Model (COM) so applications can be written in nearly any language.</span></span> <span data-ttu-id="daa54-113">Wenn Sie zusätzliche Informationen zu com benötigen, wenden Sie sich an das Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="daa54-113">If you require additional information on COM, please consult the Platform Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="daa54-114">Die von Telefoniedienstanbietern (TSPS) bereitgestellte Telefon Steuerung, die Transport spezifische Mechanismen implementiert.</span><span class="sxs-lookup"><span data-stu-id="daa54-114">Call control provided by Telephony Service Providers (TSPs), which implement transport-specific mechanisms.</span></span>
-   <span data-ttu-id="daa54-115">Mediensteuer Element, das von Media Service Providers (MSPs) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="daa54-115">Media control provided by Media Service providers (MSPs).</span></span> <span data-ttu-id="daa54-116">Aktuelle MSPs verwenden DirectShow.</span><span class="sxs-lookup"><span data-stu-id="daa54-116">Current MSPs use DirectShow.</span></span> <span data-ttu-id="daa54-117">DirectShow ist ein modulares System aus austauschbaren Komponenten, die als Filter bezeichnet werden und in einer Konfiguration mit dem Namen Filter Diagramm angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="daa54-117">DirectShow is a modular system of pluggable components called filters, arranged in a configuration called a filter graph.</span></span> <span data-ttu-id="daa54-118">Der Filter Graph-Manager überwacht die Verbindung dieser Filter und steuert den Datenfluss des Streams.</span><span class="sxs-lookup"><span data-stu-id="daa54-118">The filter graph manager oversees the connection of these filters and controls the stream's data flow.</span></span> <span data-ttu-id="daa54-119">Wenn Sie weitere Informationen zu DirectShow benötigen, wenden Sie sich an das Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="daa54-119">If you require additional information on DirectShow, please consult the Platform SDK.</span></span>

 

 



