---
title: Remoteprozeduraufruf
description: Der Microsoft-Remote Prozedur Aufruf (RPC) definiert eine leistungsstarke Technologie zum Erstellen verteilter Client-/Serverprogramme.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC (siehe Remote Prozedur Aufruf)
- Remote Prozedur Aufruf RPC, Startseite
- RPC für Remote Prozedur Aufruf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390832"
---
# <a name="remote-procedure-call"></a><span data-ttu-id="2f306-107">Remoteprozeduraufruf</span><span class="sxs-lookup"><span data-stu-id="2f306-107">Remote Procedure Call</span></span>

## <a name="purpose"></a><span data-ttu-id="2f306-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="2f306-108">Purpose</span></span>

<span data-ttu-id="2f306-109">Der Microsoft-Remote Prozedur Aufruf (RPC) definiert eine leistungsstarke Technologie zum Erstellen verteilter Client-/Serverprogramme.</span><span class="sxs-lookup"><span data-stu-id="2f306-109">Microsoft Remote Procedure Call (RPC) defines a powerful technology for creating distributed client/server programs.</span></span> <span data-ttu-id="2f306-110">Die RPC-laufzeitstubvorgänge und-Bibliotheken verwalten die meisten Prozesse im Zusammenhang mit Netzwerkprotokollen und-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="2f306-110">The RPC run-time stubs and libraries manage most of the processes relating to network protocols and communication.</span></span> <span data-ttu-id="2f306-111">Dies ermöglicht es Ihnen, sich auf die Details der Anwendung und nicht auf die Details des Netzwerks zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="2f306-111">This enables you to focus on the details of the application rather than the details of the network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="2f306-112">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="2f306-112">Where applicable</span></span>

<span data-ttu-id="2f306-113">RPC kann in allen Client/Server-Anwendungen verwendet werden, die auf Windows-Betriebssystemen basieren.</span><span class="sxs-lookup"><span data-stu-id="2f306-113">RPC can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="2f306-114">Sie kann auch zum Erstellen von Client-und Serverprogrammen für heterogene Netzwerkumgebungen verwendet werden, die solche Betriebssysteme wie UNIX und Apple enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f306-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2f306-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="2f306-115">Developer audience</span></span>

<span data-ttu-id="2f306-116">RPC ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="2f306-116">RPC is designed to be used by C/C++ programmers.</span></span> <span data-ttu-id="2f306-117">Vertrautheit mit dem Microsoft Interface Definition Language ("Mittel l") und dem Mittell-Compiler sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2f306-117">Familiarity with the Microsoft Interface Definition Language (MIDL) and the MIDL compiler are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2f306-118">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="2f306-118">Run-time requirements</span></span>

<span data-ttu-id="2f306-119">Die RPC-Laufzeitbibliotheken sind in Windows enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f306-119">The RPC run-time libraries are included with Windows.</span></span> <span data-ttu-id="2f306-120">Die Komponenten der RPC-Entwicklungsumgebung werden installiert, wenn Sie das Microsoft Windows Software Development Kit (SDK) installieren.</span><span class="sxs-lookup"><span data-stu-id="2f306-120">The components of the RPC development environment are installed when you install the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2f306-121">Weitere Informationen finden Sie unter [Installieren der RPC-Programmierumgebung](installing-the-rpc-programming-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2f306-121">For details, see [Installing the RPC Programming Environment](installing-the-rpc-programming-environment.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f306-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2f306-122">In this section</span></span>



| <span data-ttu-id="2f306-123">Thema</span><span class="sxs-lookup"><span data-stu-id="2f306-123">Topic</span></span>                                                                           | <span data-ttu-id="2f306-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2f306-124">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f306-125">Bewährte Methoden für die RPC-Programmierung</span><span class="sxs-lookup"><span data-stu-id="2f306-125">Best RPC Programming Practices</span></span>](best-rpc-programming-practices.md)<br/> | <span data-ttu-id="2f306-126">Leitfaden zu RPC-Programmierverfahren, die Sie beim Erstellen der bestmöglichen RPC-Anwendungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2f306-126">Guidance on RPC programming practices that help create the best possible RPC applications.</span></span><br/>                            |
| [<span data-ttu-id="2f306-127">Übersicht</span><span class="sxs-lookup"><span data-stu-id="2f306-127">Overview</span></span>](overviews.md)<br/>                                            | <span data-ttu-id="2f306-128">Allgemeine Informationen zum Einbinden von RPC in Ihre Client-/Server-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2f306-128">General information about incorporating RPC into your client/server applications.</span></span><br/>                                     |
| [<span data-ttu-id="2f306-129">Verweis</span><span class="sxs-lookup"><span data-stu-id="2f306-129">Reference</span></span>](reference.md)<br/>                                           | <span data-ttu-id="2f306-130">Dokumentation zu RPC-Typen,-Funktionen und-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="2f306-130">Documentation of RPC types, functions, and constants.</span></span><br/>                                                                 |
| [<span data-ttu-id="2f306-131">RPC-NDR-Engine</span><span class="sxs-lookup"><span data-stu-id="2f306-131">RPC NDR Engine</span></span>](rpc-ndr-engine.md)<br/>                                 | <span data-ttu-id="2f306-132">Dokumentation des marshallingmoduls für RPC-und DCOM-Komponenten, der RPC-Engine (Network Data Darstellung).</span><span class="sxs-lookup"><span data-stu-id="2f306-132">Documentation of the marshaling engine for RPC and DCOM components, the RPC Network Data Representation (NDR) Engine.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2f306-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2f306-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f306-134">Microsoft Interface Definition Language (Mittel l)</span><span class="sxs-lookup"><span data-stu-id="2f306-134">Microsoft Interface Definition Language (MIDL)</span></span>](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

