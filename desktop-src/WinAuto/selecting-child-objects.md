---
title: Auswählen von untergeordneten Objekten
description: Clients wenden die Methode IAccessible accSelect an, um die Auswahl oder den Tastaturfokus unter den untergeordneten Elementen eines Objekts zu ändern. Die mit dem-Befehl angegebenen selflag-Konstanten definieren den auszuführenden Vorgang.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309496"
---
# <a name="selecting-child-objects"></a><span data-ttu-id="484c8-104">Auswählen von untergeordneten Objekten</span><span class="sxs-lookup"><span data-stu-id="484c8-104">Selecting Child Objects</span></span>

<span data-ttu-id="484c8-105">Clients wird die [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) -Methode aufgerufen, um die Auswahl oder den Tastaturfokus unter den untergeordneten Elementen eines Objekts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="484c8-105">Clients call the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method to modify selection or keyboard focus among the children in an object.</span></span> <span data-ttu-id="484c8-106">Die mit dem-Befehl angegebenen [selflag-Konstanten](selflag.md) definieren den auszuführenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="484c8-106">The [SELFLAG Constants](selflag.md) specified with the call define the operation to perform.</span></span>

<span data-ttu-id="484c8-107">Wenn [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) mit dem [**selflag-Flag \_ TakeFocus**](selflag.md) für ein untergeordnetes Objekt mit einem **HWND** aufgerufen wird, wird das Flag nur wirksam, wenn das übergeordnete Objekt den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="484c8-107">If [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) is called with the [**SELFLAG\_TAKEFOCUS**](selflag.md) flag on a child object that has an **HWND**, the flag takes effect only if the object's parent has the focus.</span></span>

## <a name="performing-complex-selection-operations"></a><span data-ttu-id="484c8-108">Ausführen komplexer Auswahl Vorgänge</span><span class="sxs-lookup"><span data-stu-id="484c8-108">Performing Complex Selection Operations</span></span>

<span data-ttu-id="484c8-109">Im folgenden wird beschrieben, welche selflag-Werte beim Aufrufen von [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) angegeben werden, um komplexe Auswahl Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="484c8-109">The following describes which SELFLAG values to specify when calling [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) to perform complex selection operations.</span></span>

<span data-ttu-id="484c8-110">**So simulieren Sie einen Klick**</span><span class="sxs-lookup"><span data-stu-id="484c8-110">**To simulate a click**</span></span>

-   <span data-ttu-id="484c8-111">[**Selflag \_ "TakeFocus**](selflag.md) \| [ **selflag \_ TakeSelection** "](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="484c8-111">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_TAKESELECTION**](selflag.md)</span></span>

<span data-ttu-id="484c8-112">**So wählen Sie ein Ziel Element durch Simulieren von Strg + Klick aus**</span><span class="sxs-lookup"><span data-stu-id="484c8-112">**To select a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="484c8-113">[**Selflag \_ Start Fokus**](selflag.md) \| [ **selflag \_ AddSelection**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="484c8-113">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_ADDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="484c8-114">**So brechen Sie die Auswahl eines Ziel Elements durch Simulieren von Strg + Klick ab**</span><span class="sxs-lookup"><span data-stu-id="484c8-114">**To cancel selection of a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="484c8-115">[**Selflag \_ Start Fokus**](selflag.md) \| [ **selflag \_ RemoveSelection**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="484c8-115">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_REMOVESELECTION**](selflag.md)</span></span>

<span data-ttu-id="484c8-116">**So simulieren Sie Umschalt + Klick**</span><span class="sxs-lookup"><span data-stu-id="484c8-116">**To simulate SHIFT + click**</span></span>

-   <span data-ttu-id="484c8-117">[**Selflag \_ "TakeFocus**](selflag.md) \| [ **selflag \_ ExtendSelection** "](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="484c8-117">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_EXTENDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="484c8-118">**So wählen Sie einen Bereich von Objekten aus und legen den Fokus auf das letzte Objekt**</span><span class="sxs-lookup"><span data-stu-id="484c8-118">**To select a range of objects and put focus on the last object**</span></span>

1.  <span data-ttu-id="484c8-119">Geben Sie [**selflag \_ TakeFocus**](selflag.md) für das Start Objekt an, um den Auswahl Anker festzulegen.</span><span class="sxs-lookup"><span data-stu-id="484c8-119">Specify [**SELFLAG\_TAKEFOCUS**](selflag.md) on the starting object to set the selection anchor.</span></span>
2.  <span data-ttu-id="484c8-120">Nennen [**Sie IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) erneut, und geben Sie [**selflag \_ ExtendSelection**](selflag.md) \| [**selflag \_ TakeFocus**](selflag.md) für das letzte Objekt an.</span><span class="sxs-lookup"><span data-stu-id="484c8-120">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_EXTENDSELECTION**](selflag.md) \| [**SELFLAG\_TAKEFOCUS**](selflag.md) on the last object.</span></span>

<span data-ttu-id="484c8-121">**So deaktivieren Sie alle Objekte**</span><span class="sxs-lookup"><span data-stu-id="484c8-121">**To deselect all objects**</span></span>

1.  <span data-ttu-id="484c8-122">Geben Sie [**selflag \_ TakeSelection**](selflag.md) für ein beliebiges Objekt an.</span><span class="sxs-lookup"><span data-stu-id="484c8-122">Specify [**SELFLAG\_TAKESELECTION**](selflag.md) on any object.</span></span> <span data-ttu-id="484c8-123">Mit diesem Flag werden alle ausgewählten Objekte außer der gerade ausgewählten Objekte deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="484c8-123">This flag deselects all selected objects except the one just selected.</span></span>
2.  <span data-ttu-id="484c8-124">Nennen [**Sie IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) erneut, und geben Sie [**selflag \_ RemoveSelection**](selflag.md) für das restliche Objekt an.</span><span class="sxs-lookup"><span data-stu-id="484c8-124">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_REMOVESELECTION**](selflag.md) on the remaining object.</span></span>

 

 




