---
description: Windows-Eigenschaftensystem
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Windows-Eigenschaftensystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49e44c988d3a91572be1b42d5fbaf75e664d7f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089878"
---
# <a name="windows-property-system"></a><span data-ttu-id="29fb0-103">Windows-Eigenschaftensystem</span><span class="sxs-lookup"><span data-stu-id="29fb0-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="29fb0-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="29fb0-104">Purpose</span></span>

<span data-ttu-id="29fb0-105">Der Windows-Eigenschaftensystem ist ein erweiterbares Lese-/Schreibsystem von Datendefinitionen, das eine einheitliche Möglichkeit bietet, Metadaten zu Shellelementen auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="29fb0-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="29fb0-106">Mit dem Windows-Eigenschaftensystem in Windows Vista und höher können Sie Metadaten für Shell-Elemente speichern und abrufen.</span><span class="sxs-lookup"><span data-stu-id="29fb0-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="29fb0-107">Ein Shellelement ist ein beliebiger Einzelner Inhalt, z. B. eine Datei, ein Ordner, eine E-Mail oder ein Kontakt.</span><span class="sxs-lookup"><span data-stu-id="29fb0-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="29fb0-108">Eine Eigenschaft ist ein einzelnes Metadatenelement, das einem Shellelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="29fb0-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="29fb0-109">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="29fb0-109">Developer audience</span></span>

<span data-ttu-id="29fb0-110">Bevor Sie mit dem Lesen der Windows-Eigenschaftensystem SDK-Dokumentation beginnen, sollten Sie über grundlegende Kenntnisse der folgenden Punkte verfügen:</span><span class="sxs-lookup"><span data-stu-id="29fb0-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="29fb0-111">Component Object Model (COM)</span><span class="sxs-lookup"><span data-stu-id="29fb0-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="29fb0-112">Programmierung von Shellnamespaces</span><span class="sxs-lookup"><span data-stu-id="29fb0-112">Shell Namespace programming</span></span>

<span data-ttu-id="29fb0-113">Eine Einführung in COM finden Sie unter [COM-Grundlagen.](../com/com-fundamentals.md)</span><span class="sxs-lookup"><span data-stu-id="29fb0-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="29fb0-114">Eine Einführung in die Programmierung von Shellnamespaces finden Sie unter [Erste Schritte mit dem Shellnamespace](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="29fb0-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="29fb0-115">Informationen zur Verwendung der Windows-Eigenschaftensystem finden Sie unter [Übersicht über das Eigenschaftensystem: Entwicklungsszenarien.](property-system-overview.md)</span><span class="sxs-lookup"><span data-stu-id="29fb0-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="29fb0-116">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="29fb0-116">Run-time requirements</span></span>

<span data-ttu-id="29fb0-117">Die unterstützte Laufzeitumgebung für die Verwendung des Windows-Eigenschaftensystem ist Windows Vista oder höher und die Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="29fb0-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="29fb0-118">Windows XP und Microsoft Windows Desktop Search (WDS) 3.0 oder höher enthalten auch eine Teilmenge der Windows-Eigenschaftensystem.</span><span class="sxs-lookup"><span data-stu-id="29fb0-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="29fb0-119">Informationen zum Herunterladen des Windows 7- oder aktualisierten Windows Vista SDK finden Sie im [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="29fb0-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="29fb0-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="29fb0-120">In this section</span></span>

-   [<span data-ttu-id="29fb0-121">Übersicht über das Eigenschaftensystem</span><span class="sxs-lookup"><span data-stu-id="29fb0-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="29fb0-122">entwicklerhandbuch für Windows-Eigenschaftensystem</span><span class="sxs-lookup"><span data-stu-id="29fb0-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="29fb0-123">Referenz zum Eigenschaftensystem</span><span class="sxs-lookup"><span data-stu-id="29fb0-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="29fb0-124">Eigenschaftensystem-Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="29fb0-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
