---
title: IDXCoreAdapter
description: Die **idxcoreadapter**-   Schnittstelle implementiert Methoden zum Abrufen von Details zu einem Adapter Element.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0930ce76353d556f7839f476ec8979823eac3a6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102194"
---
# <a name="idxcoreadapter-interface"></a><span data-ttu-id="a03fb-103">Idxcoreadapter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a03fb-103">IDXCoreAdapter interface</span></span>

<span data-ttu-id="a03fb-104">Die **idxcoreadapter**-   Schnittstelle implementiert Methoden zum Abrufen von Details zu einem Adapter Element.</span><span class="sxs-lookup"><span data-stu-id="a03fb-104">The **IDXCoreAdapter** interface implements methods for retrieving details about an adapter item.</span></span> <span data-ttu-id="a03fb-105">**Idxcoreadapter** erbt von der [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a03fb-105">**IDXCoreAdapter** inherits from the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a03fb-106">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="a03fb-106">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a03fb-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a03fb-107">Remarks</span></span>

<span data-ttu-id="a03fb-108">Die Eigenschaften eines Adapters werden zu dem Zeitpunkt eingerichtet, zu dem der Adapter startet, und sind für die Lebensdauer des Adapters unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="a03fb-108">An adapter's properties are established at the time the adapter starts, and they're immutable for the lifetime of the adapter.</span></span> <span data-ttu-id="a03fb-109">Dies steht im Gegensatz zum Zustand eines Adapters, der abgefragt oder festgelegt werden kann, und die Werte von, die sich im Laufe der Zeit ändern können.</span><span class="sxs-lookup"><span data-stu-id="a03fb-109">This is in contrast to an adapter's state, which can be queried or set, and the values of which can change over time.</span></span>

## <a name="see-also"></a><span data-ttu-id="a03fb-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a03fb-110">See also</span></span>

<span data-ttu-id="a03fb-111">[DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="a03fb-111">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>