---
description: Die getFloatValue-Methode ruft einen Gleit Komma Wert (Typ VT R4) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Iportabledevicevalues:: getFloatValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364688"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a><span data-ttu-id="0e9b3-103">Iportabledevicevalues:: getFloatValue-Methode</span><span class="sxs-lookup"><span data-stu-id="0e9b3-103">IPortableDeviceValues::GetFloatValue method</span></span>

<span data-ttu-id="0e9b3-104">Die **getFloatValue** -Methode **Ruft einen Gleit** Komma Wert (Typ VT R4) ab, der \_ durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-104">The **GetFloatValue** method retrieves a **FLOAT** value (type VT\_R4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e9b3-105">Syntax</span></span>


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="0e9b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e9b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9b3-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e9b3-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9b3-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0e9b3-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0e9b3-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e9b3-110">Zeiger auf den abgerufenen **float** -Wert.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-110">Pointer to the retrieved **FLOAT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9b3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e9b3-111">Return value</span></span>

<span data-ttu-id="0e9b3-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0e9b3-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0e9b3-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0e9b3-114">Return code</span></span>                                                                                             | <span data-ttu-id="0e9b3-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e9b3-115">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e9b3-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e9b3-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="0e9b3-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="0e9b3-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="0e9b3-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>    | <span data-ttu-id="0e9b3-119">Die von *Key* angegebene Eigenschaft ist kein **float** -Typ.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-119">The property specified by *key* is not a **FLOAT** type.</span></span><br/>  |
| <dl> <span data-ttu-id="0e9b3-120"><dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="0e9b3-120"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="0e9b3-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0e9b3-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0e9b3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e9b3-122">Requirements</span></span>



| <span data-ttu-id="0e9b3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e9b3-123">Requirement</span></span> | <span data-ttu-id="0e9b3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0e9b3-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9b3-125">Header</span><span class="sxs-lookup"><span data-stu-id="0e9b3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0e9b3-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e9b3-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e9b3-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e9b3-127">Library</span></span><br/> | <dl> <span data-ttu-id="0e9b3-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e9b3-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e9b3-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e9b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e9b3-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0e9b3-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="0e9b3-131">**Iportabledebug:: setfloatvalue**</span><span class="sxs-lookup"><span data-stu-id="0e9b3-131">**IPortableDeviceValues::SetFloatValue**</span></span>](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




