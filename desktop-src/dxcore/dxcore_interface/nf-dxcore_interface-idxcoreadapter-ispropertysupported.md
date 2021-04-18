---
title: IDXCoreAdapter::IsPropertySupported
description: Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem (OS) die angegebene Adapter Eigenschaft unterstützen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338675"
---
# <a name="idxcoreadapterispropertysupported-method"></a><span data-ttu-id="da6a9-103">Idxcoreadapter:: ispropertysupported-Methode</span><span class="sxs-lookup"><span data-stu-id="da6a9-103">IDXCoreAdapter::IsPropertySupported method</span></span>

<span data-ttu-id="da6a9-104">Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem (OS) die angegebene Adapter Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="da6a9-104">Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span>

## <a name="syntax"></a><span data-ttu-id="da6a9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da6a9-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="da6a9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da6a9-106">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="da6a9-107">property</span><span class="sxs-lookup"><span data-stu-id="da6a9-107">property</span></span>

<span data-ttu-id="da6a9-108">Type: **[dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="da6a9-108">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="da6a9-109">Der Typ der Eigenschaft, die Sie für die Unterstützung von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="da6a9-109">The type of property that you're querying about support for.</span></span> <span data-ttu-id="da6a9-110">Weitere Informationen zu den einzelnen Adapter Eigenschaften finden Sie in der Tabelle unter [dxcoreadapterproperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="da6a9-110">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="da6a9-111">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="da6a9-111">Returns</span></span>

<span data-ttu-id="da6a9-112">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="da6a9-112">Type: **bool**</span></span>

<span data-ttu-id="da6a9-113">Gibt zurück,  `true`   Wenn dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem (OS) die angegebene Adapter Eigenschaft unterstützen.</span><span class="sxs-lookup"><span data-stu-id="da6a9-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span> <span data-ttu-id="da6a9-114">Andernfalls wird zurückgegeben  `false` .</span><span class="sxs-lookup"><span data-stu-id="da6a9-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="da6a9-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da6a9-115">See also</span></span>

<span data-ttu-id="da6a9-116">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="da6a9-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>