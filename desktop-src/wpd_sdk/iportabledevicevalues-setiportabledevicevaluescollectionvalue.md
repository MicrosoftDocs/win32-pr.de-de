---
description: Die Methode "* tiportabledevicevaluescollectionvalue" fügt einen neuen iportabledevicevaluescollection-Wert (Typ "VT \_ unknown") hinzu oder überschreibt eine vorhandene.
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: 'Iportabledevicevalues:: tportabledevicevaluescollectionvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3f0c545a4daceed75971b0e659f85d72eca6d98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373715"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="e0cce-103">Iportabledevicevalues:: endportabledevicevaluescollectionvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="e0cce-103">IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="e0cce-104">Die Methode "\* **tiportabledevicevaluescollectionvalue** " fügt einen neuen **iportabledevicevaluescollection** -Wert (Typ "VT \_ unknown") hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="e0cce-104">The **SetIPortableDeviceValuesCollectionValue** method adds a new **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0cce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0cce-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e0cce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0cce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0cce-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cce-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cce-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0cce-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="e0cce-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0cce-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0cce-110">Zeiger auf eine **iportableabvicevaluescollection** -Schnittstelle, die den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="e0cce-110">Pointer to an **IPortableDeviceValuesCollection** interface that specifies the new value.</span></span> <span data-ttu-id="e0cce-111">Das SDK kopiert einen Verweis auf die übermittelte Schnittstelle und ruft die **adressf** auf.</span><span class="sxs-lookup"><span data-stu-id="e0cce-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0cce-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0cce-112">Return value</span></span>

<span data-ttu-id="e0cce-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="e0cce-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e0cce-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0cce-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e0cce-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e0cce-115">Return code</span></span>                                                                          | <span data-ttu-id="e0cce-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0cce-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e0cce-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0cce-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e0cce-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0cce-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0cce-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0cce-119">Remarks</span></span>

<span data-ttu-id="e0cce-120">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0cce-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="e0cce-121">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="e0cce-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0cce-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0cce-122">Requirements</span></span>



| <span data-ttu-id="e0cce-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0cce-123">Requirement</span></span> | <span data-ttu-id="e0cce-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e0cce-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0cce-125">Header</span><span class="sxs-lookup"><span data-stu-id="e0cce-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e0cce-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0cce-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0cce-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0cce-127">Library</span></span><br/> | <dl> <span data-ttu-id="e0cce-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0cce-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0cce-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0cce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0cce-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e0cce-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e0cce-131">**Iportableendvicevalues:: getiportableervicevaluescollectionvalue**</span><span class="sxs-lookup"><span data-stu-id="e0cce-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




