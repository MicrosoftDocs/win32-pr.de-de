---
title: MIB-namens Struktur
description: Der Namespace für MIB-Objekt Bezeichner ist hierarchisch. Es ist so strukturiert, dass jedem verwaltbaren Objekt ein global eindeutiger Name zugewiesen werden kann.
ms.assetid: eb3c855c-b36b-4675-8df4-e11c128b2b34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d77b0cb4c64d9645f54ec7416c45ba1a4620ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037290"
---
# <a name="mib-name-tree"></a><span data-ttu-id="ac238-104">MIB-namens Struktur</span><span class="sxs-lookup"><span data-stu-id="ac238-104">MIB Name Tree</span></span>

<span data-ttu-id="ac238-105">Der Namespace für MIB-Objekt Bezeichner ist hierarchisch.</span><span class="sxs-lookup"><span data-stu-id="ac238-105">The name space for MIB object identifiers is hierarchical.</span></span> <span data-ttu-id="ac238-106">Es ist so strukturiert, dass jedem verwaltbaren Objekt ein global eindeutiger Name zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ac238-106">It is structured so that each manageable object can be assigned a globally unique name.</span></span>

<span data-ttu-id="ac238-107">Die Autorität für Teile des Namensraums wird einzelnen Organisationen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="ac238-107">Authority for parts of the name space is assigned to individual organizations.</span></span> <span data-ttu-id="ac238-108">Dadurch können Organisationen Namen zuweisen, ohne eine Internet Autorität für jede Zuweisung zu konsultieren.</span><span class="sxs-lookup"><span data-stu-id="ac238-108">This allows organizations to assign names without consulting an Internet authority for each assignment.</span></span> <span data-ttu-id="ac238-109">Der Namespace, der Microsoft zugewiesen ist, lautet z. b. 1.3.6.1.4.1.311, der in MSFT definiert ist. MIB.</span><span class="sxs-lookup"><span data-stu-id="ac238-109">For example, the name space assigned to Microsoft is 1.3.6.1.4.1.311, which is defined in MSFT.MIB.</span></span> <span data-ttu-id="ac238-110">Microsoft hat die Berechtigung, Objekten an einer beliebigen Stelle unterhalb dieses Namensraums Namen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ac238-110">Microsoft has the authority to assign names to objects anywhere below that name space.</span></span>

<span data-ttu-id="ac238-111">Der Objekt Bezeichner in der Hierarchie wird als Sequenz von subidentifiers geschrieben, beginnend am Stamm und am Ende des Objekts.</span><span class="sxs-lookup"><span data-stu-id="ac238-111">The object identifier in the hierarchy is written as a sequence of subidentifiers beginning at the root and ending at the object.</span></span> <span data-ttu-id="ac238-112">Unter Elemente werden durch einen bestimmten Zeitraum getrennt.</span><span class="sxs-lookup"><span data-stu-id="ac238-112">Subidentifiers are separated with a period.</span></span>

 

 




