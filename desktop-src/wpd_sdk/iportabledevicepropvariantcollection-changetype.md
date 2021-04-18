---
description: Die ChangeType-Methode konvertiert alle Elemente in der Auflistung in den angegebenen VarType.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'Iportabledevicepropvariantcollection:: ChangeType-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371409"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a><span data-ttu-id="6b7f1-103">Iportabledevicepropvariantcollection:: ChangeType-Methode</span><span class="sxs-lookup"><span data-stu-id="6b7f1-103">IPortableDevicePropVariantCollection::ChangeType method</span></span>

<span data-ttu-id="6b7f1-104">Die **ChangeType** -Methode konvertiert alle Elemente in der Auflistung in den angegebenen VarType.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-104">The **ChangeType** method converts all items in the collection to the specified VARTYPE.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b7f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b7f1-105">Syntax</span></span>


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a><span data-ttu-id="6b7f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b7f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b7f1-107">*VT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b7f1-107">*vt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b7f1-108">Gibt den **VarType** an, in den alle Elemente in der Auflistung konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-108">Specifies the **VARTYPE** to which you want to convert all items in the collection.</span></span> <span data-ttu-id="6b7f1-109">Beispiel Typen sind VT \_ UI4 und VT \_ UI8.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-109">Example types include VT\_UI4 and VT\_UI8.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b7f1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b7f1-110">Return value</span></span>

<span data-ttu-id="6b7f1-111">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6b7f1-112">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6b7f1-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b7f1-113">Return code</span></span>                                                                          | <span data-ttu-id="6b7f1-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b7f1-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6b7f1-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b7f1-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6b7f1-116">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b7f1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b7f1-117">Remarks</span></span>

<span data-ttu-id="6b7f1-118">Wenn diese Methode fehlschlägt, kann die Auflistung in einem Zwischenzustand belassen werden, wobei einige Elemente konvertiert und einige nicht konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="6b7f1-118">If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b7f1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b7f1-119">Requirements</span></span>



| <span data-ttu-id="6b7f1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b7f1-120">Requirement</span></span> | <span data-ttu-id="6b7f1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6b7f1-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b7f1-122">Header</span><span class="sxs-lookup"><span data-stu-id="6b7f1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6b7f1-123"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b7f1-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b7f1-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b7f1-124">Library</span></span><br/> | <dl> <span data-ttu-id="6b7f1-125"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b7f1-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b7f1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b7f1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b7f1-127">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6b7f1-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




