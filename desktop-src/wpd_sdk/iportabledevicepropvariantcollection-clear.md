---
description: Durch die Clear-Methode werden alle Elemente aus der Auflistung freigegeben und dann entfernt. Nach dem Aufrufen dieser Methode wird die Auflistung als leer betrachtet.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'Iportabledevicepropvariantcollection:: Clear-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359679"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a><span data-ttu-id="1faf7-104">Iportabledevicepropvariantcollection:: Clear-Methode</span><span class="sxs-lookup"><span data-stu-id="1faf7-104">IPortableDevicePropVariantCollection::Clear method</span></span>

<span data-ttu-id="1faf7-105">Durch die Clear-Methode werden alle Elemente aus der Auflistung **frei** gegeben und dann entfernt.</span><span class="sxs-lookup"><span data-stu-id="1faf7-105">The **Clear** method frees, and then removes, all items from the collection.</span></span> <span data-ttu-id="1faf7-106">Nach dem Aufrufen dieser Methode wird die Auflistung als leer betrachtet.</span><span class="sxs-lookup"><span data-stu-id="1faf7-106">The collection is considered empty after calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1faf7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1faf7-107">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="1faf7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1faf7-108">Parameters</span></span>

<span data-ttu-id="1faf7-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1faf7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1faf7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1faf7-110">Return value</span></span>

<span data-ttu-id="1faf7-111">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="1faf7-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1faf7-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1faf7-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1faf7-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1faf7-113">Return code</span></span>                                                                          | <span data-ttu-id="1faf7-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1faf7-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1faf7-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1faf7-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1faf7-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1faf7-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1faf7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1faf7-117">Remarks</span></span>

<span data-ttu-id="1faf7-118">Nach dem Aufrufen von **Clear** wird die-Auflistung als Typ-less angesehen, was bedeutet, dass der VarType, auf den Sie zuvor festgelegt wurde, keine **hinzufüge** Vorgänge einschränkt.</span><span class="sxs-lookup"><span data-stu-id="1faf7-118">After calling **Clear**, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting **Add** operations.</span></span> <span data-ttu-id="1faf7-119">Ein Aufruf zum **Hinzufügen** nach dem Aufrufen von **Clear** wird als "First"- **Add** für diese Auflistung betrachtet.</span><span class="sxs-lookup"><span data-stu-id="1faf7-119">A call to **Add** after calling **Clear** is considered the "first" **Add** for this collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="1faf7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1faf7-120">Requirements</span></span>



| <span data-ttu-id="1faf7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1faf7-121">Requirement</span></span> | <span data-ttu-id="1faf7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1faf7-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faf7-123">Header</span><span class="sxs-lookup"><span data-stu-id="1faf7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1faf7-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="1faf7-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1faf7-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1faf7-125">Library</span></span><br/> | <dl> <span data-ttu-id="1faf7-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1faf7-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1faf7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1faf7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1faf7-128">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1faf7-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




