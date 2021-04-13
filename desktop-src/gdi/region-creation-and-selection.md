---
description: Eine Anwendung erstellt durch Aufrufen einer Funktion, die einer bestimmten Form zugeordnet ist, einen Bereich. In der folgenden Tabelle werden die Funktionen angezeigt, die den einzelnen Standardformen zugeordnet sind.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Regionale Erstellung und-Auswahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978352"
---
# <a name="region-creation-and-selection"></a><span data-ttu-id="d889e-104">Regionale Erstellung und-Auswahl</span><span class="sxs-lookup"><span data-stu-id="d889e-104">Region Creation and Selection</span></span>

<span data-ttu-id="d889e-105">Eine Anwendung erstellt durch Aufrufen einer Funktion, die einer bestimmten Form zugeordnet ist, einen Bereich.</span><span class="sxs-lookup"><span data-stu-id="d889e-105">An application creates a region by calling a function associated with a specific shape.</span></span> <span data-ttu-id="d889e-106">In der folgenden Tabelle werden die Funktionen angezeigt, die den einzelnen Standardformen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d889e-106">The following table shows the function(s) associated with each of the standard shapes.</span></span>



| <span data-ttu-id="d889e-107">Form</span><span class="sxs-lookup"><span data-stu-id="d889e-107">Shape</span></span>                                   | <span data-ttu-id="d889e-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="d889e-108">Function</span></span>                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d889e-109">Rechteckiger Bereich</span><span class="sxs-lookup"><span data-stu-id="d889e-109">Rectangular region</span></span>                      | <span data-ttu-id="d889e-110">" [**Kreaterectrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)", " [**kreaterectrgnindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)", " [**setrectrgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) "</span><span class="sxs-lookup"><span data-stu-id="d889e-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span></span> |
| <span data-ttu-id="d889e-111">Rechteckiger Bereich mit abgerundeten Ecken</span><span class="sxs-lookup"><span data-stu-id="d889e-111">Rectangular region with rounded corners</span></span> | [<span data-ttu-id="d889e-112">**"Kreateroundrectrgn"**</span><span class="sxs-lookup"><span data-stu-id="d889e-112">**CreateRoundRectRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| <span data-ttu-id="d889e-113">Elliptische Region</span><span class="sxs-lookup"><span data-stu-id="d889e-113">Elliptical region</span></span>                       | <span data-ttu-id="d889e-114">" [**Kreateellipticrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)", " [ **kreateellipticrgnindirekte** "](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span><span class="sxs-lookup"><span data-stu-id="d889e-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span></span>                   |
| <span data-ttu-id="d889e-115">Polygonaler Bereich</span><span class="sxs-lookup"><span data-stu-id="d889e-115">Polygonal region</span></span>                        | <span data-ttu-id="d889e-116">" [**Kreatepolygonrgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)", " [ **kreatepolypolygonrgn** "](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span><span class="sxs-lookup"><span data-stu-id="d889e-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span></span>                               |



 

<span data-ttu-id="d889e-117">Jede Regions Erstellungs Funktion gibt ein Handle zurück, das den neuen Bereich identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d889e-117">Each region creation function returns a handle that identifies the new region.</span></span> <span data-ttu-id="d889e-118">Eine Anwendung kann dieses Handle verwenden, um den Bereich in einen Gerätekontext auszuwählen, indem die [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) -Funktion aufgerufen und dieses Handle als zweites Argument bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d889e-118">An application can use this handle to select the region into a device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function and supplying this handle as the second argument.</span></span> <span data-ttu-id="d889e-119">Nachdem ein Bereich in einen Gerätekontext ausgewählt wurde, kann die Anwendung verschiedene Vorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="d889e-119">After a region is selected into a device context, the application can perform various operations on it.</span></span>

 

 



