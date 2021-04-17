---
title: IDXCoreAdapter::IsAttributeSupported
description: Bestimmt, ob dieses DXCore-Adapter Objekt das angegebene Adapter Attribut unterstützt.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390461"
---
# <a name="idxcoreadapterisattributesupported-method"></a><span data-ttu-id="b92d7-103">Idxcoreadapter:: isattributesupportiert-Methode</span><span class="sxs-lookup"><span data-stu-id="b92d7-103">IDXCoreAdapter::IsAttributeSupported method</span></span>

<span data-ttu-id="b92d7-104">Bestimmt, ob dieses DXCore-Adapter Objekt das angegebene Adapter Attribut unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b92d7-104">Determines whether this DXCore adapter object supports the specified adapter attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="b92d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b92d7-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a><span data-ttu-id="b92d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b92d7-106">Parameters</span></span>

### <a name="attributeguid"></a><span data-ttu-id="b92d7-107">attributeguid</span><span class="sxs-lookup"><span data-stu-id="b92d7-107">attributeGUID</span></span>

<span data-ttu-id="b92d7-108">Typ: **reguid**</span><span class="sxs-lookup"><span data-stu-id="b92d7-108">Type: **REFGUID**</span></span>

<span data-ttu-id="b92d7-109">Ein Verweis auf eine GUID des Adapter Attributs.</span><span class="sxs-lookup"><span data-stu-id="b92d7-109">A reference to an adapter attribute GUID.</span></span> <span data-ttu-id="b92d7-110">Eine Liste der Attribut-GUIDs finden Sie unter [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b92d7-110">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span>

## <a name="returns"></a><span data-ttu-id="b92d7-111">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="b92d7-111">Returns</span></span>

<span data-ttu-id="b92d7-112">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="b92d7-112">Type: **bool**</span></span>

<span data-ttu-id="b92d7-113">Gibt zurück,  `true`   Wenn dieses DXCore-Adapter Objekt das angegebene Adapter Attribut unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b92d7-113">Returns `true` if this DXCore adapter object supports the specified adapter attribute.</span></span> <span data-ttu-id="b92d7-114">Andernfalls wird zurückgegeben  `false` .</span><span class="sxs-lookup"><span data-stu-id="b92d7-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="b92d7-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b92d7-115">See also</span></span>

<span data-ttu-id="b92d7-116">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b92d7-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>