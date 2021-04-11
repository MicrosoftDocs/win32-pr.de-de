---
description: Die IP Helper-API (Internet Protocol Helper) ermöglicht das Abrufen und Ändern von Netzwerk Konfigurationseinstellungen für den lokalen Computer.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: IP-Hilfsprogramm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862447"
---
# <a name="ip-helper"></a><span data-ttu-id="a6d1a-103">IP-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="a6d1a-103">IP Helper</span></span>

## <a name="purpose"></a><span data-ttu-id="a6d1a-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="a6d1a-104">Purpose</span></span>

<span data-ttu-id="a6d1a-105">Die IP Helper-API (Internet Protocol Helper) ermöglicht das Abrufen und Ändern von Netzwerk Konfigurationseinstellungen für den lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-105">The Internet Protocol Helper (IP Helper) API enables the retrieval and modification of network configuration settings for the local computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a6d1a-106">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="a6d1a-106">Where applicable</span></span>

<span data-ttu-id="a6d1a-107">Die IP-hilfsprogrammapi ist in jeder Computerumgebung anwendbar, in der die programmgesteuerte Bearbeitung der Netzwerk-und TCP/IP-Konfiguration nützlich ist.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-107">The IP Helper API is applicable in any computing environment where programmatically manipulating network and TCP/IP configuration is useful.</span></span> <span data-ttu-id="a6d1a-108">Typische Anwendungen sind IP-Routing Protokolle und SNMP (Simple Network Management Protocol)-Agents.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-108">Typical applications include IP routing protocols and Simple Network Management Protocol (SNMP) agents.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a6d1a-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="a6d1a-109">Developer audience</span></span>

<span data-ttu-id="a6d1a-110">Die IP Helper-API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-110">The IP Helper API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="a6d1a-111">Programmierer sollten auch mit den Konzepten von Windows-Netzwerken und TCP/IP-Netzwerken vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-111">Programmers should also be familiar with Windows networking and TCP/IP networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a6d1a-112">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="a6d1a-112">Run-time requirements</span></span>

<span data-ttu-id="a6d1a-113">Die IP-hilfsprogrammapi kann auf allen Windows-Plattformen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-113">The IP Helper API can be used on all Windows platforms.</span></span> <span data-ttu-id="a6d1a-114">Nicht alle Betriebssysteme unterstützen alle Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-114">Not all operating systems support all functions.</span></span> <span data-ttu-id="a6d1a-115">Wenn bestimmte Implementierungen oder Funktionen von Windows Sockets 2-Platt Form Einschränkungen vorhanden sind, sind Sie in der Dokumentation eindeutig angegeben.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-115">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span> <span data-ttu-id="a6d1a-116">Wenn eine IP-Hilfsfunktion auf einer Plattform aufgerufen wird, die die Funktion nicht unterstützt, wird "Error \_ Not \_ supported" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-116">If an IP Helper function is called on a platform that does not support the function, ERROR\_NOT\_SUPPORTED is returned.</span></span> <span data-ttu-id="a6d1a-117">Spezifischere Informationen dazu, welche Betriebssysteme eine bestimmte Funktion unterstützen, finden Sie in den Abschnitten zu den Anforderungen in der-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-117">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a6d1a-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a6d1a-118">In this section</span></span>



| <span data-ttu-id="a6d1a-119">Thema</span><span class="sxs-lookup"><span data-stu-id="a6d1a-119">Topic</span></span>                                                              | <span data-ttu-id="a6d1a-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6d1a-120">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6d1a-121">Neues in IP Helper</span><span class="sxs-lookup"><span data-stu-id="a6d1a-121">What's New in IP Helper</span></span>](what-s-new-in-ip-helper.md)<br/>  | <span data-ttu-id="a6d1a-122">Informationen zu neuen Features für das IP-Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-122">Information on new features for IP Helper.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="a6d1a-123">Info</span><span class="sxs-lookup"><span data-stu-id="a6d1a-123">About IP Helper</span></span>](about-ip-helper.md)<br/>                  | <span data-ttu-id="a6d1a-124">Allgemeine Informationen zu den Überlegungen und Funktionen der IP-Hilfsprogrammen für Entwickler.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-124">General information about IP Helper programming considerations and capabilities available to developers.</span></span><br/>                                                                                               |
| [<span data-ttu-id="a6d1a-125">Verwenden von IP Helper</span><span class="sxs-lookup"><span data-stu-id="a6d1a-125">Using IP Helper</span></span>](using-ip-helper.md)<br/>                  | <span data-ttu-id="a6d1a-126">Prozeduren und Programmiertechniken, die mit IP Helper verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-126">Procedures and programming techniques used with IP Helper.</span></span> <span data-ttu-id="a6d1a-127">Dieser Abschnitt enthält grundlegende Programmiertechniken für IP-Hilfsprogramme, wie z. b. die ersten Schritte [mit IP Helper](getting-started-with-ip-helper.md).</span><span class="sxs-lookup"><span data-stu-id="a6d1a-127">This section includes basic IP Helper programming techniques, such as [Getting Started With IP Helper](getting-started-with-ip-helper.md).</span></span><br/> |
| [<span data-ttu-id="a6d1a-128">Referenz zum IP-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="a6d1a-128">IP Helper reference</span></span>](ip-helper-function-reference.md)<br/> | <span data-ttu-id="a6d1a-129">Referenz Dokumentation für die IP-Hilfsobjekte, Strukturen und Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="a6d1a-129">Reference documentation for the IP Helper functions, structures, and enumerations.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="a6d1a-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6d1a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6d1a-131">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="a6d1a-131">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="a6d1a-132">Routing- und RAS-Dienst</span><span class="sxs-lookup"><span data-stu-id="a6d1a-132">Routing and Remote Access Service</span></span>](../rras/routing-start-page.md)
</dt> </dl>

 

