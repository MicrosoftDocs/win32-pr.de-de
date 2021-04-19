---
description: Die Methode "* tiportabledevicekeycollectionvalue" fügt einen neuen Wert für "stiportabledevicekeycollectionvalue" (Typ "VT \_ unknown") hinzu oder überschreibt eine vorhandene.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'Iportabledevicevalues:: tportabledevicekeycollectionvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366973"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="30ed1-103">Iportabledevicevalues:: endportabledevicekeycollectionvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="30ed1-103">IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="30ed1-104">Die Methode "\* **tiportabledevicekeycollectionvalue** " fügt einen neuen Wert für " **stiportabledevicekeycollectionvalue** " (Typ "VT \_ unknown") hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="30ed1-104">The **SetIPortableDeviceKeyCollectionValue** method adds a new **SetIPortableDeviceKeyCollectionValue** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ed1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30ed1-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="30ed1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30ed1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ed1-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30ed1-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ed1-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="30ed1-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="30ed1-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30ed1-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ed1-110">Zeiger auf eine **iportabledevicekeycollection** -Schnittstelle, die den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="30ed1-110">Pointer to an **IPortableDeviceKeyCollection** interface that specifies the new value.</span></span> <span data-ttu-id="30ed1-111">Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft die **adressf** auf.</span><span class="sxs-lookup"><span data-stu-id="30ed1-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ed1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30ed1-112">Return value</span></span>

<span data-ttu-id="30ed1-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="30ed1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="30ed1-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30ed1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="30ed1-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="30ed1-115">Return code</span></span>                                                                          | <span data-ttu-id="30ed1-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30ed1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="30ed1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30ed1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="30ed1-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30ed1-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30ed1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30ed1-119">Remarks</span></span>

<span data-ttu-id="30ed1-120">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="30ed1-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="30ed1-121">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="30ed1-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="30ed1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30ed1-122">Requirements</span></span>



| <span data-ttu-id="30ed1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30ed1-123">Requirement</span></span> | <span data-ttu-id="30ed1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="30ed1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ed1-125">Header</span><span class="sxs-lookup"><span data-stu-id="30ed1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="30ed1-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="30ed1-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="30ed1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30ed1-127">Library</span></span><br/> | <dl> <span data-ttu-id="30ed1-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30ed1-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30ed1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30ed1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ed1-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="30ed1-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="30ed1-131">**Iportablede vicevalues:: getiportabledevicekeycollectionvalue**</span><span class="sxs-lookup"><span data-stu-id="30ed1-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




