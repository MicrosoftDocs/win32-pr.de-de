---
title: IDXCoreAdapterList::IsStale
description: Bestimmt, ob Änderungen an diesem System dazu geführt haben, dass dieses DXCore-Adapter Listen Objekt veraltet geworden ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68b4e4ba6f3434f76ea5b4a2a98ae4e83486f61e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340527"
---
# <a name="idxcoreadapterlistisstale-method"></a><span data-ttu-id="a0773-103">Idxcoreadapterlist:: isstale-Methode</span><span class="sxs-lookup"><span data-stu-id="a0773-103">IDXCoreAdapterList::IsStale method</span></span>

<span data-ttu-id="a0773-104">Bestimmt, ob Änderungen an diesem System dazu geführt haben, dass dieses DXCore-Adapter Listen Objekt veraltet geworden ist.</span><span class="sxs-lookup"><span data-stu-id="a0773-104">Determines whether changes to this system have resulted in this DXCore adapter list object becoming out of date.</span></span> <span data-ttu-id="a0773-105">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="a0773-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0773-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0773-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a><span data-ttu-id="a0773-107">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="a0773-107">Returns</span></span>

<span data-ttu-id="a0773-108">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="a0773-108">Type: **bool**</span></span>

<span data-ttu-id="a0773-109">Gibt zurück,  `true`   Wenn bei der Erstellung der Liste Änderungen an den Systembedingungen aufgetreten sind, die dazu geführt haben, dass diese Adapter Liste veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a0773-109">Returns `true` if, since generating the list, changes to system conditions have occurred that would cause this adapter list to become stale.</span></span> <span data-ttu-id="a0773-110">Andernfalls wird zurückgegeben  `false` .</span><span class="sxs-lookup"><span data-stu-id="a0773-110">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0773-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0773-111">Remarks</span></span>

<span data-ttu-id="a0773-112">Sie können " **isstale** " Abfragen, um zu bestimmen, ob eine Änderung der Systembedingungen dazu geführt hat, dass diese Liste veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="a0773-112">You can poll **IsStale** to determine whether changing system conditions have led to this list becoming out of date.</span></span> <span data-ttu-id="a0773-113">Wenn **isstale** einmal zurückgibt `true` , wird `true` für die verbleibende Lebensdauer des DXCore-Adapter Listen Objekts zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0773-113">If **IsStale** returns `true` once, then it returns `true` for the remaining lifetime of the DXCore adapter list object.</span></span> <span data-ttu-id="a0773-114">Ein veraltetes Listen Objekt wird weiterhin als veraltet eingestuft, auch wenn die Systembedingungen zu einem Status zurückkehren, der der Liste entspricht (die gleichen Bedingungen werden nun wie bei der ersten Generierung der Liste abgerufen).</span><span class="sxs-lookup"><span data-stu-id="a0773-114">A stale list object is still considered stale even if system conditions return to a state that matches the list (the same conditions obtain now as did when the list was first generated).</span></span>

## <a name="see-also"></a><span data-ttu-id="a0773-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0773-115">See also</span></span>

<span data-ttu-id="a0773-116">[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a0773-116">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>