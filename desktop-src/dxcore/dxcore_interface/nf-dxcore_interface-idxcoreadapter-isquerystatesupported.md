---
title: IDXCoreAdapter::IsQueryStateSupported
description: Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem die Abfrage des Werts des angegebenen Adapter Zustands unterstützen.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102042"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a><span data-ttu-id="cdc07-103">Idxcoreadapter:: isquerystaatupportiert-Methode</span><span class="sxs-lookup"><span data-stu-id="cdc07-103">IDXCoreAdapter::IsQueryStateSupported method</span></span>

<span data-ttu-id="cdc07-104">Bestimmt, ob dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem die Abfrage des Werts des angegebenen Adapter Zustands unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cdc07-104">Determines whether this DXCore adapter object and the current operating system (OS) support querying the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdc07-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="cdc07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdc07-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="cdc07-107">state</span><span class="sxs-lookup"><span data-stu-id="cdc07-107">state</span></span>

<span data-ttu-id="cdc07-108">Typ: **[dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="cdc07-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="cdc07-109">Die Art des Zustands Elements, das Sie für die Unterstützung von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="cdc07-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="cdc07-110">Weitere Informationen zu den einzelnen adapterstatusarten finden Sie in der Tabelle unter [dxcoreadapterstate](./ne-dxcore_interface-dxcoreadapterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc07-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="cdc07-111">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="cdc07-111">Returns</span></span>

<span data-ttu-id="cdc07-112">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="cdc07-112">Type: **bool**</span></span>

<span data-ttu-id="cdc07-113">Gibt zurück,  `true`   Wenn dieses DXCore-Adapter Objekt und das aktuelle Betriebssystem die Abfrage des angegebenen Adapter Zustands unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cdc07-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support querying the specified adapter state.</span></span> <span data-ttu-id="cdc07-114">Andernfalls wird zurückgegeben  `false` .</span><span class="sxs-lookup"><span data-stu-id="cdc07-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdc07-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc07-115">See also</span></span>

<span data-ttu-id="cdc07-116">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="cdc07-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>