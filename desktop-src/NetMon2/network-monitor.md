---
description: Netzwerkmonitor erfasst Netzwerk Datenverkehr für die Anzeige und Analyse. Es ermöglicht Ihnen das Ausführen von Aufgaben wie z. b. das Analysieren zuvor erfasster Daten in benutzerdefinierten Methoden und das Extrahieren von Daten aus definierten Protokoll Parser.
ms.assetid: a70b6e22-e744-4760-b878-9ee35428fed5
title: Netzwerkmonitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51a57dd2373d7a10fedd68a72dbc4021efdb921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529744"
---
# <a name="network-monitor"></a><span data-ttu-id="42669-104">Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="42669-104">Network Monitor</span></span>

## <a name="purpose"></a><span data-ttu-id="42669-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="42669-105">Purpose</span></span>

<span data-ttu-id="42669-106">Netzwerkmonitor erfasst Netzwerk Datenverkehr für die Anzeige und Analyse.</span><span class="sxs-lookup"><span data-stu-id="42669-106">Network Monitor captures network traffic for display and analysis.</span></span> <span data-ttu-id="42669-107">Es ermöglicht Ihnen das Ausführen von Aufgaben wie z. b. das Analysieren zuvor erfasster Daten in benutzerdefinierten Methoden und das Extrahieren von Daten aus definierten Protokoll Parser.</span><span class="sxs-lookup"><span data-stu-id="42669-107">It enables you to perform tasks such as analyzing previously captured data in user-defined methods and extract data from defined protocol parsers.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="42669-108">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="42669-108">Developer audience</span></span>

<span data-ttu-id="42669-109">Auf alle von Netzwerkmonitor bereitgestellten API-Sätze kann mithilfe von C/C++ zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="42669-109">All API sets provided by Network Monitor can be accessed using C/C++.</span></span> <span data-ttu-id="42669-110">Entwickler, die mit [*Netzwerk Paket Anbietern*](n.md) arbeiten, müssen auch mit com vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="42669-110">Those developers also working with [*network packet providers*](n.md) must also be familiar with COM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="42669-111">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="42669-111">Run-time requirements</span></span>

<span data-ttu-id="42669-112">Um die Netzwerkmonitor-API aufzurufen, müssen Sie unter Windows NT Server 4,0, Windows 2000 Server oder Windows Server 2003 oder Microsoft Systems Management Server installiert sein.</span><span class="sxs-lookup"><span data-stu-id="42669-112">To call from the Network Monitor API, you must be running on Windows NT Server 4.0, Windows 2000 Server, or Windows Server 2003, or have Microsoft Systems Management Server installed.</span></span>

<span data-ttu-id="42669-113">Der NPP-Treiber und die unterstützten Funktionen umfassen alle Versionen von Windows NT 4,0 und Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="42669-113">The NPP driver and supported features include all versions of Windows NT 4.0 and Windows 2000 Server.</span></span>

> [!Note]  
> <span data-ttu-id="42669-114">Netzwerkmonitor 2,1 und frühere Versionen werden unter Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42669-114">Network Monitor 2.1 and earlier are not supported on Windows Vista and later.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="42669-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="42669-115">In this section</span></span>



| <span data-ttu-id="42669-116">Thema</span><span class="sxs-lookup"><span data-stu-id="42669-116">Topic</span></span>                                                                 | <span data-ttu-id="42669-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42669-117">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="42669-118">Das Netzwerkmonitor SDK</span><span class="sxs-lookup"><span data-stu-id="42669-118">The Network Monitor SDK</span></span>](the-network-monitor-sdk.md)<br/>     | <span data-ttu-id="42669-119">Einführung in das Netzwerkmonitor SDK.</span><span class="sxs-lookup"><span data-stu-id="42669-119">Introduction to the Network Monitor SDK.</span></span><br/>                                                   |
| [<span data-ttu-id="42669-120">Informationen zu Netzwerkmonitor 2,1</span><span class="sxs-lookup"><span data-stu-id="42669-120">About Network Monitor 2.1</span></span>](about-network-monitor-2-1.md)<br/> | <span data-ttu-id="42669-121">Netzwerkmonitor-Konzepte und-Dienste.</span><span class="sxs-lookup"><span data-stu-id="42669-121">Network Monitor concepts and services.</span></span><br/>                                                     |
| [<span data-ttu-id="42669-122">Verwenden von Netzwerkmonitor 2,1</span><span class="sxs-lookup"><span data-stu-id="42669-122">Using Network Monitor 2.1</span></span>](using-network-monitor-2-1.md)<br/> | <span data-ttu-id="42669-123">Aufgabenbezogene Themen, in denen beschrieben wird, wie Netzwerkmonitor Funktionen und COM-Komponenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42669-123">Task-related topics that describe how to use Network Monitor functions and COM components.</span></span><br/> |
| [<span data-ttu-id="42669-124">Verweis</span><span class="sxs-lookup"><span data-stu-id="42669-124">Reference</span></span>](reference.md)<br/>                                 | <span data-ttu-id="42669-125">Referenz Themen für Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="42669-125">Reference topics for Network Monitor.</span></span><br/>                                                      |
| [<span data-ttu-id="42669-126">Glossar</span><span class="sxs-lookup"><span data-stu-id="42669-126">Glossary</span></span>](glossary.md)<br/>                                   | <span data-ttu-id="42669-127">Definitionen und Terminologie für Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="42669-127">Definitions and terminology for Network Monitor.</span></span><br/>                                           |



 

 

 




