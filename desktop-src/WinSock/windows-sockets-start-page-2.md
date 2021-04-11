---
description: Mit Windows Sockets 2 (Winsock) können Programmierer Erweiterte Internet-, Intranet-und andere netzwerkfähige Anwendungen erstellen, um Anwendungsdaten über das Netzwerk hinweg unabhängig vom verwendeten Netzwerkprotokoll zu übertragen.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130409"
---
# <a name="windows-sockets-2"></a><span data-ttu-id="63b43-103">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="63b43-103">Windows Sockets 2</span></span>

## <a name="purpose"></a><span data-ttu-id="63b43-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="63b43-104">Purpose</span></span>

<span data-ttu-id="63b43-105">Mit Windows Sockets 2 (Winsock) können Programmierer Erweiterte Internet-, Intranet-und andere netzwerkfähige Anwendungen erstellen, um Anwendungsdaten über das Netzwerk hinweg unabhängig vom verwendeten Netzwerkprotokoll zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="63b43-105">Windows Sockets 2 (Winsock) enables programmers to create advanced Internet, intranet, and other network-capable applications to transmit application data across the wire, independent of the network protocol being used.</span></span> <span data-ttu-id="63b43-106">Mit Winsock erhalten Programmierer Zugriff auf Erweiterte Funktionen von Microsoft® Windows® Netzwerk, wie z. b. Multicast und Quality of Service (QoS).</span><span class="sxs-lookup"><span data-stu-id="63b43-106">With Winsock, programmers are provided access to advanced Microsoft® Windows® networking capabilities such as multicast and Quality of Service (QoS).</span></span>

<span data-ttu-id="63b43-107">Winsock folgt dem Windows Open System Architecture (WOSA)-Modell. Es definiert eine Standard-Service Provider Interface (SPI) zwischen der Anwendungsprogrammierschnittstelle (Application Programming Interface, API) mit den exportierten Funktionen und den Protokoll stapeln.</span><span class="sxs-lookup"><span data-stu-id="63b43-107">Winsock follows the Windows Open System Architecture (WOSA) model; it defines a standard service provider interface (SPI) between the application programming interface (API), with its exported functions and the protocol stacks.</span></span> <span data-ttu-id="63b43-108">Dabei wird das socketparadigma verwendet, das zuerst von der UNIX Software Distribution (BSD) UNIX populär gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="63b43-108">It uses the sockets paradigm that was first popularized by Berkeley Software Distribution (BSD) UNIX.</span></span> <span data-ttu-id="63b43-109">Es wurde später für Windows in Windows Sockets 1,1 angepasst, mit dem Windows Sockets 2-Anwendungen abwärts kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="63b43-109">It was later adapted for Windows in Windows Sockets 1.1, with which Windows Sockets 2 applications are backward compatible.</span></span> <span data-ttu-id="63b43-110">Winsock-Programmierung, die zuvor um TCP/IP zentriert war.</span><span class="sxs-lookup"><span data-stu-id="63b43-110">Winsock programming previously centered around TCP/IP.</span></span> <span data-ttu-id="63b43-111">Einige Programmierpraktiken, die mit TCP/IP funktionieren, funktionieren nicht bei jedem Protokoll.</span><span class="sxs-lookup"><span data-stu-id="63b43-111">Some programming practices that worked with TCP/IP do not work with every protocol.</span></span> <span data-ttu-id="63b43-112">Folglich werden von der Windows Sockets 2-API bei Bedarf Funktionen zum Verarbeiten mehrerer Protokolle hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="63b43-112">As a result, the Windows Sockets 2 API adds functions where necessary to handle several protocols.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="63b43-113">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="63b43-113">Developer audience</span></span>

<span data-ttu-id="63b43-114">Windows Sockets 2 ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="63b43-114">Windows Sockets 2 is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="63b43-115">Vertrautheit mit Windows-Netzwerken ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="63b43-115">Familiarity with Windows networking is required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="63b43-116">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="63b43-116">Run-time requirements</span></span>

<span data-ttu-id="63b43-117">Windows Sockets 2 kann auf allen Windows-Plattformen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63b43-117">Windows Sockets 2 can be used on all Windows platforms.</span></span> <span data-ttu-id="63b43-118">Wenn bestimmte Implementierungen oder Funktionen von Windows Sockets 2-Platt Form Einschränkungen vorhanden sind, sind Sie in der Dokumentation eindeutig angegeben.</span><span class="sxs-lookup"><span data-stu-id="63b43-118">Where certain implementations or capabilities of Windows Sockets 2 platform restrictions do exist, they are clearly noted in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="63b43-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="63b43-119">In this section</span></span>



| <span data-ttu-id="63b43-120">Thema</span><span class="sxs-lookup"><span data-stu-id="63b43-120">Topic</span></span>                                                                                             | <span data-ttu-id="63b43-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63b43-121">Description</span></span>                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63b43-122">Neuerungen bei Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="63b43-122">What's New for Windows Sockets</span></span>](what-s-new-for-windows-sockets-2.md)<br/>                 | <span data-ttu-id="63b43-123">Informationen zu neuen Features für Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="63b43-123">Information on new features for Windows Sockets.</span></span><br/>                                                                                                                                                                                                                                 |
| [<span data-ttu-id="63b43-124">Winsock-Netzwerkprotokoll Unterstützung in Windows</span><span class="sxs-lookup"><span data-stu-id="63b43-124">Winsock Network Protocol Support in Windows</span></span>](network-protocol-support-in-windows.md)<br/> | <span data-ttu-id="63b43-125">Informationen zur Unterstützung von Netzwerkprotokollen für Windows Sockets unter verschiedenen Windows-Versionen.</span><span class="sxs-lookup"><span data-stu-id="63b43-125">Information on network protocol support for Windows Sockets on different versions of Windows.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="63b43-126">Informationen zu Winsock</span><span class="sxs-lookup"><span data-stu-id="63b43-126">About Winsock</span></span>](about-winsock.md)<br/>                                                     | <span data-ttu-id="63b43-127">Allgemeine Informationen zu den Überlegungen, zur Architektur und zu den Funktionen von Windows Sockets, die Entwicklern zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="63b43-127">General information on Windows Sockets programming considerations, architecture, and capabilities available to developers.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="63b43-128">Verwenden von Winsock</span><span class="sxs-lookup"><span data-stu-id="63b43-128">Using Winsock</span></span>](using-winsock.md)<br/>                                                     | <span data-ttu-id="63b43-129">Prozeduren und Programmiertechniken, die mit Windows Sockets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63b43-129">Procedures and programming techniques used with Windows Sockets.</span></span> <span data-ttu-id="63b43-130">Dieser Abschnitt enthält grundlegende Winsock-Programmiertechniken, wie z. b. die ersten Schritte [mit Winsock](getting-started-with-winsock.md), sowie erweiterte Techniken, die für erfahrene Winsock-Entwickler nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="63b43-130">This section includes basic Winsock programming techniques, such as [Getting Started With Winsock](getting-started-with-winsock.md), as well as advanced techniques useful for experienced Winsock developers.</span></span><br/> |
| [<span data-ttu-id="63b43-131">Winsock-Referenz</span><span class="sxs-lookup"><span data-stu-id="63b43-131">Winsock Reference</span></span>](winsock-reference.md)<br/>                                             | <span data-ttu-id="63b43-132">Dokumentation der Windows Sockets-API.</span><span class="sxs-lookup"><span data-stu-id="63b43-132">Documentation of the Windows Sockets API.</span></span><br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="63b43-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63b43-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63b43-134">IP-Hilfsdienst</span><span class="sxs-lookup"><span data-stu-id="63b43-134">IP Helper</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="63b43-135">Quality of Service (QoS, Dienstqualität)</span><span class="sxs-lookup"><span data-stu-id="63b43-135">Quality of Service</span></span>](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
