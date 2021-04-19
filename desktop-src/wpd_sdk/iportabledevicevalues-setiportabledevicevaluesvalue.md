---
description: Die Methode "* tiportabledevicevaluesvalue" fügt einen neuen iportabledevicevalues-Wert hinzu (Type VT \_ unknown) oder überschreibt eine vorhandene.
ms.assetid: 3e51964e-6ee0-4885-94ca-cc8000b456b4
title: 'Iportabledevicevalues:: tportabledevicevaluesvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 265a5d3633dfa8252ff7afd4042a41e476040d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372330"
---
# <a name="iportabledevicevaluessetiportabledevicevaluesvalue-method"></a><span data-ttu-id="5c251-103">Iportabledevicevalues:: endportabledevicevaluesvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="5c251-103">IPortableDeviceValues::SetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="5c251-104">Die Methode "\* **tiportabledevicevaluesvalue** " fügt einen neuen **iportabledevicevalues** -Wert hinzu (Type VT \_ unknown) oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="5c251-104">The **SetIPortableDeviceValuesValue** method adds a new **IPortableDeviceValues** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c251-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c251-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesValue(
  [in] REFPROPERTYKEY        key,
  [in] IPortableDeviceValues *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="5c251-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c251-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c251-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c251-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c251-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c251-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="5c251-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c251-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c251-110">Ein Zeiger auf eine **iportablede vicevalues** -Schnittstelle, die den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="5c251-110">Pointer to an **IPortableDeviceValues** interface that specifies the new value.</span></span> <span data-ttu-id="5c251-111">Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft die **adressf** auf.</span><span class="sxs-lookup"><span data-stu-id="5c251-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c251-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c251-112">Return value</span></span>

<span data-ttu-id="5c251-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5c251-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c251-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5c251-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c251-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5c251-115">Return code</span></span>                                                                          | <span data-ttu-id="5c251-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c251-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5c251-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c251-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5c251-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c251-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c251-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c251-119">Remarks</span></span>

<span data-ttu-id="5c251-120">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="5c251-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="5c251-121">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="5c251-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c251-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c251-122">Requirements</span></span>



| <span data-ttu-id="5c251-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c251-123">Requirement</span></span> | <span data-ttu-id="5c251-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5c251-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c251-125">Header</span><span class="sxs-lookup"><span data-stu-id="5c251-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5c251-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c251-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c251-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5c251-127">Library</span></span><br/> | <dl> <span data-ttu-id="5c251-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c251-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c251-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c251-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c251-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5c251-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="5c251-131">**Iportableendvicevalues:: getiportableendvicevaluesvalue**</span><span class="sxs-lookup"><span data-stu-id="5c251-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-getiportabledevicevaluesvalue.md)
</dt> </dl>

 

 




