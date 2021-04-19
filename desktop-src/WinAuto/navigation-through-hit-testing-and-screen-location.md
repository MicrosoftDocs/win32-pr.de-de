---
title: Navigation durch Treffer Tests und Bildschirmposition
description: Um die untergeordneten Elemente eines Objekts zu suchen oder die Größe eines Objekts zu ermitteln, können Clients auf dem Bildschirm auf Testpunkte zugreifen.
ms.assetid: ba08814f-87bc-4b47-8b61-179a48d5092f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26d055246e038611e881bd353bcc865c5e77136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341443"
---
# <a name="navigation-through-hit-testing-and-screen-location"></a><span data-ttu-id="c0917-103">Navigation durch Treffer Tests und Bildschirmposition</span><span class="sxs-lookup"><span data-stu-id="c0917-103">Navigation Through Hit Testing and Screen Location</span></span>

<span data-ttu-id="c0917-104">Um die untergeordneten Elemente eines Objekts zu suchen oder die Größe eines Objekts zu ermitteln, können Clients auf dem Bildschirm auf Testpunkte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c0917-104">To locate an object's children or to determine an object's size, clients can hit test points on the screen.</span></span> <span data-ttu-id="c0917-105">Es stehen zwei Methoden zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="c0917-105">Two methods are available:</span></span>

-   [<span data-ttu-id="c0917-106">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="c0917-106">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="c0917-107">**IAccessible:: accLocation**</span><span class="sxs-lookup"><span data-stu-id="c0917-107">**IAccessible::accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="using-iaccessibleacchittest"></a><span data-ttu-id="c0917-108">Verwenden von IAccessible:: accHitTest</span><span class="sxs-lookup"><span data-stu-id="c0917-108">Using IAccessible::accHitTest</span></span>

<span data-ttu-id="c0917-109">Um zu ermitteln, ob sich ein Punkt innerhalb eines Objekts innerhalb seines untergeordneten Elements befindet, wird die [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) -Methode des übergeordneten Objekts aufgerufen, und die Bildschirm Koordinaten des Punkts, der auf Treffer getestet werden soll, werden übergeben.</span><span class="sxs-lookup"><span data-stu-id="c0917-109">To identify whether a point is within an object, within its child, or neither, clients call the [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) method of the parent object, passing the screen coordinates of the point to be hit tested.</span></span> <span data-ttu-id="c0917-110">In der folgenden Liste werden einige typische Szenarien beschrieben:</span><span class="sxs-lookup"><span data-stu-id="c0917-110">The following list describes some typical scenarios:</span></span>

-   <span data-ttu-id="c0917-111">Wenn die untergeordneten Elemente des Objekts sich an einem angegebenen Punkt überlappen, ruft [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) das oberste untergeordnete Element ab, das visuell angezeigt wird, um den Bereich zu belegen.</span><span class="sxs-lookup"><span data-stu-id="c0917-111">If the object's children overlap at a specified point, [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) retrieves the topmost child that visually appears to occupy the space.</span></span>
-   <span data-ttu-id="c0917-112">Wenn ein Fenster ein untergeordnetes Element abdeckt oder wenn das untergeordnete Element durch das übergeordnete Element abgeschnitten wird, wird beim durch Klicken auf den abgedeckten Punkt das untergeordnete Element abgerufen, auch wenn es nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="c0917-112">If a window covers a child, or if the child is clipped by the parent, hit testing the covered point retrieves the child even though it is not visible.</span></span>
-   <span data-ttu-id="c0917-113">Wenn das am angegebenen Punkt gefundene untergeordnete Element ein Barrierefreies Objekt ist, und nicht auf ein untergeordnetes Element, gibt die Methode die [**IDispatch**](idispatch-interface.md) -Schnittstelle des untergeordneten Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="c0917-113">If the child found at the specified point is an accessible object, as opposed to a child element, the method returns the child's [**IDispatch**](idispatch-interface.md) interface.</span></span>

## <a name="using-iaccessibleacclocation"></a><span data-ttu-id="c0917-114">Verwenden von IAccessible:: accLocation</span><span class="sxs-lookup"><span data-stu-id="c0917-114">Using IAccessible::accLocation</span></span>

<span data-ttu-id="c0917-115">Um die Bildschirmposition eines Objekts oder eines der untergeordneten Elemente des Objekts abzurufen, wird " [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)" aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c0917-115">To get the screen location of an object or one of the object's children, clients call [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).</span></span> <span data-ttu-id="c0917-116">Diese Methode gibt die Koordinaten des umgebenden Rechtecks des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="c0917-116">This method returns the coordinates of the specified object's bounding rectangle.</span></span> <span data-ttu-id="c0917-117">Wenn das Objekt nicht wie ein Rechteck geformt ist, gibt die Methode die Koordinaten des kleinsten Rechtecks zurück, das das gesamte Objekt umfasst.</span><span class="sxs-lookup"><span data-stu-id="c0917-117">If the object is not shaped like a rectangle, the method returns the coordinates of the smallest rectangle that encompasses the entire object.</span></span>

<span data-ttu-id="c0917-118">Die folgende Abbildung zeigt die Beziehung zwischen dem Bereich eines nicht rechteckigen Objekts und seinem umschließenden Rechteck.</span><span class="sxs-lookup"><span data-stu-id="c0917-118">The following illustration shows the relationship between a non-rectangular object's region and its bounding rectangle.</span></span>

![Abbildung der Darstellung eines nicht rechteckigen Objekts (eines Kreises) und seines umschließenden Rechtecks.](images/region.gif)

> [!Note]  
> <span data-ttu-id="c0917-120">[**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) ist präziser als [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , da Clients den Speicherort von Objekten auf Pixel-für-Pixel-Basis anstelle von Begrenzungs Rechtecke ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="c0917-120">[**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) is more precise than [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because it enables clients to determine the location of objects on a pixel-by-pixel basis rather than with bounding rectangles.</span></span> <span data-ttu-id="c0917-121">Diese Genauigkeit ist beispielsweise hilfreich, wenn eine Anwendung Informationen durch Nachverfolgung der Position des Mauszeigers sammelt.</span><span class="sxs-lookup"><span data-stu-id="c0917-121">This precision is useful, for example, when an application is gathering information by tracking the location of the mouse pointer.</span></span>

 

 

 




