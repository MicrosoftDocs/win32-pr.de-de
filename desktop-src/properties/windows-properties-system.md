---
description: .
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Windows-Eigenschaften System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e96f931d37ef698339f9219a0dc8db43a6003e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343268"
---
# <a name="windows-property-system"></a><span data-ttu-id="69ba8-103">Windows-Eigenschaften System</span><span class="sxs-lookup"><span data-stu-id="69ba8-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="69ba8-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="69ba8-104">Purpose</span></span>

<span data-ttu-id="69ba8-105">Das Windows-Eigenschaften System ist ein erweiterbares Lese-/Schreibsystem mit Daten Definitionen, das eine einheitliche Methode zum Ausdrücken von Metadaten über shellelemente bietet.</span><span class="sxs-lookup"><span data-stu-id="69ba8-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="69ba8-106">Mit dem Windows-Eigenschaften System in Windows Vista und höher können Sie Metadaten für shellelemente speichern und abrufen.</span><span class="sxs-lookup"><span data-stu-id="69ba8-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="69ba8-107">Ein shellelement ist ein beliebiges einzelnes Element, z. b. eine Datei, ein Ordner, eine e-Mail oder ein Kontakt.</span><span class="sxs-lookup"><span data-stu-id="69ba8-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="69ba8-108">Eine Eigenschaft ist ein einzelner Metadatenelement, das einem shellelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="69ba8-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="69ba8-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="69ba8-109">Developer audience</span></span>

<span data-ttu-id="69ba8-110">Bevor Sie mit dem Lesen der Windows-System-SDK-Dokumentation beginnen, sollten Sie über grundlegende Kenntnisse der folgenden Kenntnisse verfügen:</span><span class="sxs-lookup"><span data-stu-id="69ba8-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="69ba8-111">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="69ba8-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="69ba8-112">Shell-Namespace Programmierung</span><span class="sxs-lookup"><span data-stu-id="69ba8-112">Shell Namespace programming</span></span>

<span data-ttu-id="69ba8-113">Eine Einführung in com finden Sie unter [com-Grundlagen](../com/com-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="69ba8-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="69ba8-114">Eine Einführung in die Programmierung von Shell-Namespaces finden Sie unter [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="69ba8-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="69ba8-115">Informationen zur Verwendung des Windows-Eigenschaften Systems finden Sie unter [Übersicht über das Eigenschaften System: Entwicklungsszenarien](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="69ba8-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="69ba8-116">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="69ba8-116">Run-time requirements</span></span>

<span data-ttu-id="69ba8-117">Die unterstützte Laufzeitumgebung für die Verwendung des Windows-Eigenschaften Systems ist Windows Vista oder höher und das Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="69ba8-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="69ba8-118">Windows XP und Microsoft Windows Desktop Search (WDS) 3,0 oder höher enthalten ebenfalls eine Teilmenge des Windows-Eigenschaften Systems.</span><span class="sxs-lookup"><span data-stu-id="69ba8-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="69ba8-119">Informationen zum Herunterladen von Windows 7 oder zum aktualisierten Windows Vista SDK finden Sie in der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="69ba8-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69ba8-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="69ba8-120">In this section</span></span>

-   [<span data-ttu-id="69ba8-121">Übersicht über das Eigenschaftensystem</span><span class="sxs-lookup"><span data-stu-id="69ba8-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="69ba8-122">Entwicklerhandbuch für Windows-Eigenschaften System</span><span class="sxs-lookup"><span data-stu-id="69ba8-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="69ba8-123">Eigenschaften System Referenz</span><span class="sxs-lookup"><span data-stu-id="69ba8-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="69ba8-124">Eigenschaftensystem-Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="69ba8-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
