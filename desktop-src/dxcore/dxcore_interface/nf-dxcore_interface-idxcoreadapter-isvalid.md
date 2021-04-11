---
title: IDXCoreAdapter::IsValid
description: Bestimmt, ob dieses DXCore-Adapter Objekt noch gültig ist.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039368"
---
# <a name="idxcoreadapterisvalid-method"></a><span data-ttu-id="88a2a-103">Idxcoreadapter:: IsValid-Methode</span><span class="sxs-lookup"><span data-stu-id="88a2a-103">IDXCoreAdapter::IsValid method</span></span>

<span data-ttu-id="88a2a-104">Bestimmt, ob dieses DXCore-Adapter Objekt noch gültig ist.</span><span class="sxs-lookup"><span data-stu-id="88a2a-104">Determines whether this DXCore adapter object is still valid.</span></span> <span data-ttu-id="88a2a-105">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="88a2a-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="88a2a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="88a2a-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a><span data-ttu-id="88a2a-107">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="88a2a-107">Returns</span></span>

<span data-ttu-id="88a2a-108">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="88a2a-108">Type: **bool**</span></span>

<span data-ttu-id="88a2a-109">Gibt zurück,  `true`   Wenn dieses DXCore-Adapter Objekt noch gültig ist.</span><span class="sxs-lookup"><span data-stu-id="88a2a-109">Returns `true` if this DXCore adapter object is still valid.</span></span> <span data-ttu-id="88a2a-110">Andernfalls wird zurückgegeben  `false` .</span><span class="sxs-lookup"><span data-stu-id="88a2a-110">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="88a2a-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88a2a-111">See also</span></span>

<span data-ttu-id="88a2a-112">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="88a2a-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>