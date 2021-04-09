---
description: Erweitert Anwendungen, die mithilfe von COM-basierten Technologien geschrieben wurden.
ms.assetid: b21a6b08-c17c-4fcc-bc60-39037bc9902f
title: Com+ (Komponenten Dienste)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b778c31957ddfe3f71db23b2f5be2a3ee681fde0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958356"
---
# <a name="com-component-services"></a><span data-ttu-id="016c6-103">Com+ (Komponenten Dienste)</span><span class="sxs-lookup"><span data-stu-id="016c6-103">COM+ (Component Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="016c6-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="016c6-104">Purpose</span></span>

<span data-ttu-id="016c6-105">Com+ ist eine Weiterentwicklung von Microsoft Component Object Model (com) und Microsoft Transaction Server (MTS).</span><span class="sxs-lookup"><span data-stu-id="016c6-105">COM+ is an evolution of Microsoft Component Object Model (COM) and Microsoft Transaction Server (MTS).</span></span> <span data-ttu-id="016c6-106">Com+ baut auf Anwendungen auf und erweitert Anwendungen, die mithilfe von com, MTS und anderen COM-basierten Technologien geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="016c6-106">COM+ builds on and extends applications written using COM, MTS, and other COM-based technologies.</span></span> <span data-ttu-id="016c6-107">Com+ verarbeitet viele der Ressourcen Verwaltungsaufgaben, die Sie zuvor selbst programmieren mussten, wie z. b. Thread Zuordnung und Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="016c6-107">COM+ handles many of the resource management tasks that you previously had to program yourself, such as thread allocation and security.</span></span> <span data-ttu-id="016c6-108">Mit com+ können Sie Ihre Anwendungen auch skalierbarer machen, indem Sie Thread Pooling, Objekt Pooling und Just-in-Time-Objekt Aktivierung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="016c6-108">COM+ also makes your applications more scalable by providing thread pooling, object pooling, and just-in-time object activation.</span></span> <span data-ttu-id="016c6-109">Com+ trägt auch dazu bei, die Integrität Ihrer Daten zu schützen, indem Transaktionsunterstützung bereitgestellt wird, auch wenn eine Transaktion mehrere Datenbanken über ein Netzwerk umfasst.</span><span class="sxs-lookup"><span data-stu-id="016c6-109">COM+ also helps protect the integrity of your data by providing transaction support, even if a transaction spans multiple databases over a network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="016c6-110">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="016c6-110">Where applicable</span></span>

<span data-ttu-id="016c6-111">Com+ kann verwendet werden, um unternehmensweite, unternehmenskritische, verteilte Anwendungen für Windows zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="016c6-111">COM+ can be used to develop enterprise-wide, mission-critical, distributed applications for Windows.</span></span>

<span data-ttu-id="016c6-112">Wenn Sie ein Systemadministrator sind, werden Sie com+-Anwendungen und deren Komponenten installieren, bereitstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="016c6-112">If you are a system administrator, you will be installing, deploying, and configuring COM+ applications and their components.</span></span> <span data-ttu-id="016c6-113">Wenn Sie Programmierer der Anwendung sind, schreiben Sie Komponenten und integrieren Sie als Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="016c6-113">If you are an application programmer, you will be writing components and integrating them as applications.</span></span> <span data-ttu-id="016c6-114">Wenn Sie ein Tool Anbieter sind, entwickeln oder ändern Sie Tools für die Arbeit in der com+-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="016c6-114">If you are a tools vendor, you will be developing or modifying tools to work in the COM+ environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="016c6-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="016c6-115">Developer audience</span></span>

<span data-ttu-id="016c6-116">Com+ wurde hauptsächlich für Microsoft Visual C++-und Microsoft Visual Basic-Entwickler entwickelt.</span><span class="sxs-lookup"><span data-stu-id="016c6-116">COM+ is designed primarily for Microsoft Visual C++ and Microsoft Visual Basic developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="016c6-117">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="016c6-117">Run-time requirements</span></span>

<span data-ttu-id="016c6-118">Die com+-Version 1,5 ist in Windows ab Windows XP und Windows Server 2003 enthalten.</span><span class="sxs-lookup"><span data-stu-id="016c6-118">COM+ version 1.5 is included in Windows starting with Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="016c6-119">Die com+-Version 1,0 ist in Windows 2000 enthalten.</span><span class="sxs-lookup"><span data-stu-id="016c6-119">COM+ version 1.0 is included in Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="016c6-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="016c6-120">In this section</span></span>

-   [<span data-ttu-id="016c6-121">Neues in com+ 1,5</span><span class="sxs-lookup"><span data-stu-id="016c6-121">What's New in COM+ 1.5</span></span>](what-s-new-in-com--1-5.md)
-   [<span data-ttu-id="016c6-122">Übersicht über com+-Entwickler</span><span class="sxs-lookup"><span data-stu-id="016c6-122">COM+ Developers Overview</span></span>](com--developers-overview.md)
-   [<span data-ttu-id="016c6-123">Com+-Dienste</span><span class="sxs-lookup"><span data-stu-id="016c6-123">COM+ Services</span></span>](com--services.md)
-   [<span data-ttu-id="016c6-124">Allgemeine com+-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="016c6-124">COM+ General Tasks</span></span>](com--general-tasks.md)
-   [<span data-ttu-id="016c6-125">Com+-Referenz</span><span class="sxs-lookup"><span data-stu-id="016c6-125">COM+ Reference</span></span>](com--reference.md)

## <a name="related-topics"></a><span data-ttu-id="016c6-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="016c6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="016c6-127">COM</span><span class="sxs-lookup"><span data-stu-id="016c6-127">COM</span></span>](/windows/desktop/com/component-object-model--com--portal)
</dt> </dl>

 

 
