---
description: Die GetType-Methode ruft den Datentyp der Elemente in der Auflistung ab.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Iportabledevicepropvariantcollection:: GetType-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365976"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a><span data-ttu-id="75354-103">Iportabledevicepropvariantcollection:: GetType-Methode</span><span class="sxs-lookup"><span data-stu-id="75354-103">IPortableDevicePropVariantCollection::GetType method</span></span>

<span data-ttu-id="75354-104">Die **GetType** -Methode ruft den Datentyp der Elemente in der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="75354-104">The **GetType** method retrieves the data type of the items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75354-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="75354-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a><span data-ttu-id="75354-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75354-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75354-107">*Pvt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75354-107">*pvt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75354-108">Ein Platform SDK- **VarType** -Enumerationswert, der den Datentyp aller Elemente in der Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="75354-108">A Platform SDK **VARTYPE** enumeration value that indicates the data type of all the items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75354-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75354-109">Return value</span></span>

<span data-ttu-id="75354-110">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="75354-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="75354-111">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="75354-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="75354-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="75354-112">Return code</span></span>                                                                               | <span data-ttu-id="75354-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75354-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="75354-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="75354-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="75354-115">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75354-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="75354-116"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="75354-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="75354-117">Ein erforderliches Zeigerargument war **null**.</span><span class="sxs-lookup"><span data-stu-id="75354-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75354-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75354-118">Remarks</span></span>

<span data-ttu-id="75354-119">Alle Elemente, die in einer **iportabledevicepropvariantcollection** gespeichert sind, weisen denselben Typ auf.</span><span class="sxs-lookup"><span data-stu-id="75354-119">All items that are stored in an **IPortableDevicePropVariantCollection** are the same type.</span></span>

## <a name="requirements"></a><span data-ttu-id="75354-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75354-120">Requirements</span></span>



| <span data-ttu-id="75354-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75354-121">Requirement</span></span> | <span data-ttu-id="75354-122">Wert</span><span class="sxs-lookup"><span data-stu-id="75354-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75354-123">Header</span><span class="sxs-lookup"><span data-stu-id="75354-123">Header</span></span><br/>  | <dl> <span data-ttu-id="75354-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="75354-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="75354-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75354-125">Library</span></span><br/> | <dl> <span data-ttu-id="75354-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75354-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75354-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75354-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75354-128">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="75354-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




