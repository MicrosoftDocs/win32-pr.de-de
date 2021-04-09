---
title: Systemwiederherstellung
description: Legt System Wiederherstellungspunkte fest und überwacht wichtige Systemänderungen von einem Programm, um ein Rollback des Systems in einen früheren Zustand zu ermöglichen. Schreiben Sie automatischen Wiederherstellungscode oder ein WMI-Skript, um den Systemstatus auf einem registrierten Wiederherstellungspunkt wiederherzustellen
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Systemwiederherstellung
- System Wiederherstellung, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101934"
---
# <a name="system-restore"></a><span data-ttu-id="4c77c-106">Systemwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="4c77c-106">System Restore</span></span>

## <a name="purpose"></a><span data-ttu-id="4c77c-107">Zweck</span><span class="sxs-lookup"><span data-stu-id="4c77c-107">Purpose</span></span>

<span data-ttu-id="4c77c-108">Bei der Systemwiederherstellung werden wichtige Systemänderungen auf dem Computer eines Benutzers automatisch überwacht und aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4c77c-108">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="4c77c-109">Es wurde entwickelt, um Supportkosten zu senken und die Kundenzufriedenheit zu erhöhen, indem ein Benutzer eine Änderung rückgängig machen kann, die möglicherweise ein Problem mit dem System verursacht hat, oder bis zu einem Tag zurückgekehrt ist, an dem das System optimal funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4c77c-109">It is designed to reduce support costs and increase customer satisfaction by enabling a user to undo a change that may have caused a problem with the system, or revert to a day when the system was performing optimally.</span></span>

> [!Note]  
> <span data-ttu-id="4c77c-110">Die folgende Dokumentation ist für Entwickler bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4c77c-110">The following documentation is targeted for developers.</span></span> <span data-ttu-id="4c77c-111">Wenn Sie ein Endbenutzer sind, der Informationen zur Verwendung der Systemwiederherstellung sucht, finden Sie weitere Informationen unter [Was ist die Systemwiederherstellung?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span><span class="sxs-lookup"><span data-stu-id="4c77c-111">If you are an end-user looking for information on how to use System Restore, see [What Is System Restore?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="4c77c-112">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="4c77c-112">Developer audience</span></span>

<span data-ttu-id="4c77c-113">Die Systemwiederherstellungs-API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="4c77c-113">The System Restore API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="4c77c-114">Eine Vertrautheit mit Windows-Verwaltungsinstrumentation (WMI) ist erforderlich, um die Skript Schnittstelle zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c77c-114">A familiarity with Windows Management Instrumentation (WMI) is required to use the scripting interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="4c77c-115">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="4c77c-115">Run-time requirements</span></span>

<span data-ttu-id="4c77c-116">Die Systemwiederherstellungs-API wird ab Windows XP auf Client Betriebssystemen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c77c-116">The System Restore API is supported on client operating systems starting with Windows XP.</span></span> <span data-ttu-id="4c77c-117">Informationen dazu, welche Betriebssysteme für die Verwendung eines bestimmten API-Elements erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der zugehörigen Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="4c77c-117">For information about which operating systems are required to use a particular API element, see the Requirements section of its documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4c77c-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4c77c-118">In this section</span></span>



| <span data-ttu-id="4c77c-119">Thema</span><span class="sxs-lookup"><span data-stu-id="4c77c-119">Topic</span></span>                                                | <span data-ttu-id="4c77c-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c77c-120">Description</span></span>                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="4c77c-121">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4c77c-121">Overview</span></span>](about-system-restore.md)<br/>      | <span data-ttu-id="4c77c-122">Eine Übersicht über die Funktionsweise der System Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="4c77c-122">An overview of how System Restore works.</span></span><br/>                            |
| [<span data-ttu-id="4c77c-123">Verweis</span><span class="sxs-lookup"><span data-stu-id="4c77c-123">Reference</span></span>](system-restore-reference.md)<br/> | <span data-ttu-id="4c77c-124">Dokumentation der Funktionen, Strukturen und Klassen der System Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="4c77c-124">Documentation of System Restore functions, structures, and classes.</span></span><br/> |
| [<span data-ttu-id="4c77c-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c77c-125">Samples</span></span>](using-system-restore.md)<br/>       | <span data-ttu-id="4c77c-126">Ein Beispielprogramm, das in C geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="4c77c-126">A sample program written in C.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="4c77c-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c77c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c77c-128">WMI</span><span class="sxs-lookup"><span data-stu-id="4c77c-128">WMI</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

