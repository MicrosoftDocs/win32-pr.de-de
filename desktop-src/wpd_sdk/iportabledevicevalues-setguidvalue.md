---
description: Die setguidvalue-Methode fügt einen neuen GUID-Wert (Type VT \_ CLSID) hinzu oder überschreibt einen vorhandenen GUID-Wert.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'Iportabledevicevalues:: setguidvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9d9f85def6ba487163f7c4c7d7441a89e0747ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351332"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a><span data-ttu-id="ef1db-103">Iportabledevicevalues:: setguidvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="ef1db-103">IPortableDeviceValues::SetGuidValue method</span></span>

<span data-ttu-id="ef1db-104">Die **setguidvalue** -Methode fügt einen neuen **GUID** -Wert (Type VT \_ CLSID) hinzu oder überschreibt einen vorhandenen GUID-Wert.</span><span class="sxs-lookup"><span data-stu-id="ef1db-104">The **SetGuidValue** method adds a new **GUID** value (type VT\_CLSID) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef1db-105">Syntax</span></span>


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
);
```



## <a name="parameters"></a><span data-ttu-id="ef1db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef1db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1db-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef1db-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1db-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef1db-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ef1db-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef1db-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1db-110">Eine **reguid** , die den neuen Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="ef1db-110">A **REFGUID** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1db-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef1db-111">Return value</span></span>

<span data-ttu-id="ef1db-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ef1db-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ef1db-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ef1db-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef1db-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef1db-114">Return code</span></span>                                                                          | <span data-ttu-id="ef1db-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef1db-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ef1db-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef1db-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ef1db-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef1db-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef1db-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef1db-118">Remarks</span></span>

<span data-ttu-id="ef1db-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef1db-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1db-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef1db-120">Requirements</span></span>



| <span data-ttu-id="ef1db-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef1db-121">Requirement</span></span> | <span data-ttu-id="ef1db-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ef1db-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1db-123">Header</span><span class="sxs-lookup"><span data-stu-id="ef1db-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ef1db-124"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef1db-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef1db-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef1db-125">Library</span></span><br/> | <dl> <span data-ttu-id="ef1db-126"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef1db-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1db-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef1db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1db-128">Hinzufügen einer Ressource zu einem Objekt</span><span class="sxs-lookup"><span data-stu-id="ef1db-128">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="ef1db-129">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ef1db-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ef1db-130">**Iportablede vicevalues:: getguidvalue**</span><span class="sxs-lookup"><span data-stu-id="ef1db-130">**IPortableDeviceValues::GetGuidValue**</span></span>](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




