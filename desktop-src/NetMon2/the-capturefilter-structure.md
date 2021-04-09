---
description: In Netzwerkmonitor wird der Erfassungs Filter durch die capturefilter-Struktur definiert.
ms.assetid: 03cd35f2-4da5-4ef6-b73f-0bf6e0e33135
title: Die capturefilter-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3962ef9828ce13a1d03c58e4d7744d2854624858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959011"
---
# <a name="the-capturefilter-structure"></a><span data-ttu-id="7bfbc-103">Die capturefilter-Struktur</span><span class="sxs-lookup"><span data-stu-id="7bfbc-103">The CAPTUREFILTER Structure</span></span>

<span data-ttu-id="7bfbc-104">In Netzwerkmonitor wird der [Erfassungs Filter](capture-filters.md) durch die [**capturefilter**](capturefilter.md) -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-104">In Network Monitor, the [capture filter](capture-filters.md) is defined by the [**CAPTUREFILTER**](capturefilter.md) structure.</span></span> <span data-ttu-id="7bfbc-105">Das Fehlen oder Kombinieren von Flags, Werten und Ausdrücken bestimmt, welche Frames von der Netzwerkmonitor-Treiber weitergegeben oder verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-105">The absence or combination of flags, values, and expressions determines which frames will be passed on or dropped by the Network Monitor driver.</span></span> <span data-ttu-id="7bfbc-106">Die folgende Abbildung zeigt die drei Bereiche der Erfassungs Filter Analyse: ETYPE/SAP, address und Pattern Match.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-106">The following illustration shows the three areas of the capture filter analysis: Etype/SAP, address, and pattern match.</span></span>

![drei Bereiche der Erfassungs Filter Analyse](images/capfilter.png)

<span data-ttu-id="7bfbc-108">In der folgenden Tabelle sind die Funktionen der einzelnen Erfassungs Filterelemente aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-108">The following table lists the function of each capture filter element.</span></span>



| <span data-ttu-id="7bfbc-109">Filter-Element</span><span class="sxs-lookup"><span data-stu-id="7bfbc-109">Filter element</span></span>                                       | <span data-ttu-id="7bfbc-110">Aktion</span><span class="sxs-lookup"><span data-stu-id="7bfbc-110">Action</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7bfbc-111">ETYPE/SAP</span><span class="sxs-lookup"><span data-stu-id="7bfbc-111">Etype/SAP</span></span>](writing-etypesap-filter-portion.md)     | <span data-ttu-id="7bfbc-112">Wertet ETYPE/SAP-Einstellungen aus.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-112">Evaluates Etype/SAP settings.</span></span> <span data-ttu-id="7bfbc-113">Die Kombination von Flags bestimmt, welche Einstellungs Typen oder-Werte eingeschlossen oder ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-113">The combination of flags determines which setting types or values are included or excluded.</span></span>                                                                                    |
| [<span data-ttu-id="7bfbc-114">Adresse</span><span class="sxs-lookup"><span data-stu-id="7bfbc-114">Address</span></span>](writing-addresstable-filter-portion.md)   | <span data-ttu-id="7bfbc-115">Wertet Quell-und Zieladressen und Adress Paare aus.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-115">Evaluates source and destination addresses and address pairs.</span></span> <span data-ttu-id="7bfbc-116">Verschiedene Kombinationen von Flags bestimmen, welche einzelnen Werte oder Kombinationen von Adress Paaren eingeschlossen oder ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-116">Different combinations of flags determine which individual values or combinations of address pairs are included or excluded.</span></span>                   |
| [<span data-ttu-id="7bfbc-117">Muster Übereinstimmung</span><span class="sxs-lookup"><span data-stu-id="7bfbc-117">Pattern Match</span></span>](writing-the-patternmatch-filter.md) | <span data-ttu-id="7bfbc-118">Definiert komplexe Muster Übereinstimmungen innerhalb eines Frames.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-118">Defines complex pattern matches within a frame.</span></span> <span data-ttu-id="7bfbc-119">Flags werden für verschiedene Typen und Offsets bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-119">Flags are provided for different types and offsets.</span></span> <span data-ttu-id="7bfbc-120">Sie können Muster Übereinstimmungen mit logischen and-oder or-Operator-Anweisungen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-120">You can combine pattern matches with logical AND or OR operator statements.</span></span>                              |
| [<span data-ttu-id="7bfbc-121">Freistellen</span><span class="sxs-lookup"><span data-stu-id="7bfbc-121">Clipping</span></span>](clipping-a-frame.md)                     | <span data-ttu-id="7bfbc-122">Schneidet Frames auf eine Weise aus, die von verschiedenen Byte Werten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-122">Clips frames in a manner specified by various byte values.</span></span> <span data-ttu-id="7bfbc-123">Sie können nur dieses Element verwenden, um alle Frames auszuschneiden oder mit anderen Erfassungs Filterelementen zu verwenden. um z. b. einen einzelnen Frame zu suchen und dann zu schneiden.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-123">You can use only this element to clip all frames or use it with other capture filter elements; for example, to find and then clip a single frame.</span></span> |
| [<span data-ttu-id="7bfbc-124">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="7bfbc-124">**Trigger**</span></span>](trigger.md)                           | <span data-ttu-id="7bfbc-125">Dieses Erfassungs Filterelement ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-125">This capture filter element is obsolete.</span></span> <span data-ttu-id="7bfbc-126">Trigger sind nicht mehr Teil eines Erfassungs Filters. Sie sind jetzt in ihren eigenen BLOB-Tags enthalten, die separat angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-126">Triggers are no longer part of a capture filter; they are now contained in their own BLOB tags, which are specified separately.</span></span>                                     |



 

<span data-ttu-id="7bfbc-127">Ein Frame wird gegen alle drei Teile des Erfassungs Filters ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-127">A frame is evaluated against all three portions of the capture filter.</span></span> <span data-ttu-id="7bfbc-128">Daher muss ein erfolgreich übertragener Frame jedes Element übergeben.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-128">Therefore, a successfully transmitted frame must pass each element.</span></span> <span data-ttu-id="7bfbc-129">Beachten Sie, dass der Netzwerkmonitor Treiber das Fehlen eines der drei Elemente als " **true**" auswertet.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-129">Be aware that the Network Monitor driver evaluates the absence of any of the three elements as **TRUE**.</span></span> <span data-ttu-id="7bfbc-130">Der Treiber wertet z. b. das Fehlen eines ETYPE/SAP-Abschnitts als "alle Frames mit einem beliebigen ETYPE/SAP-Wert sind gültig" aus.</span><span class="sxs-lookup"><span data-stu-id="7bfbc-130">For example, the driver evaluates the absence of an Etype/SAP section as "ALL frames with the ANY Etype/SAP value are valid."</span></span>

 

 



