---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Bestimmt, ob ein angegebener [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert vom Betriebssystem erkannt wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728040"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a><span data-ttu-id="c55ee-103">Idxcoreadapterlist:: isadapterpreferencesupportiert-Methode</span><span class="sxs-lookup"><span data-stu-id="c55ee-103">IDXCoreAdapterList::IsAdapterPreferenceSupported method</span></span>

## <a name="description"></a><span data-ttu-id="c55ee-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c55ee-104">Description</span></span>

<span data-ttu-id="c55ee-105">Bestimmt, ob ein angegebener [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert vom aktuellen Betriebssystem (OS) erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="c55ee-105">Determines whether a specified [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value is understood by the current operating system (OS).</span></span> <span data-ttu-id="c55ee-106">Sie können **isadapterpreferencesupportiert** aufrufen, bevor Sie [idxcoreadapterlist:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c55ee-106">You can call **IsAdapterPreferenceSupported** before calling [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c55ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c55ee-107">Syntax</span></span>

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a><span data-ttu-id="c55ee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c55ee-108">Parameters</span></span>

### <a name="preference"></a><span data-ttu-id="c55ee-109">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c55ee-109">preference</span></span>

<span data-ttu-id="c55ee-110">Typ: **[dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span><span class="sxs-lookup"><span data-stu-id="c55ee-110">Type: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**</span></span>

<span data-ttu-id="c55ee-111">Ein [dxcoreadapterpreference](./ne-dxcore_interface-dxcoreadapterpreference.md) -Wert, der geprüft wird, um festzustellen, ob er vom Betriebssystem unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c55ee-111">A [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) value that will be checked to see whether it's supported by the OS.</span></span>

## <a name="returns"></a><span data-ttu-id="c55ee-112">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="c55ee-112">Returns</span></span>

<span data-ttu-id="c55ee-113">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="c55ee-113">Type: **bool**</span></span>

<span data-ttu-id="c55ee-114">Gibt zurück, `true` Wenn der Sortierungstyp vom aktuellen Betriebssystem erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="c55ee-114">Returns `true` if the sort type is understood by the current OS.</span></span> <span data-ttu-id="c55ee-115">Andernfalls wird `false`zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c55ee-115">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="c55ee-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c55ee-116">See also</span></span>

<span data-ttu-id="c55ee-117">[Idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="c55ee-117">[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>