---
description: Die SetBoolValue-Methode fügt einen neuen booleschen Wert (Typ VT \_ bool) hinzu oder überschreibt eine vorhandene.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: 'Iportabledevicevalues:: SetBoolValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7adf311e863c08873aa8300f9e940d4a5b49417f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364848"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a><span data-ttu-id="ac80e-103">Iportabledevicevalues:: SetBoolValue-Methode</span><span class="sxs-lookup"><span data-stu-id="ac80e-103">IPortableDeviceValues::SetBoolValue method</span></span>

<span data-ttu-id="ac80e-104">Die **SetBoolValue** -Methode fügt einen neuen **booleschen** Wert (Typ VT \_ bool) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="ac80e-104">The **SetBoolValue** method adds a new **Boolean** value (type VT\_BOOL) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac80e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac80e-105">Syntax</span></span>


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
);
```



## <a name="parameters"></a><span data-ttu-id="ac80e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac80e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac80e-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac80e-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80e-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac80e-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ac80e-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac80e-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac80e-110">Ein **boolescher** Wert, der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="ac80e-110">A **BOOL** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac80e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac80e-111">Return value</span></span>

<span data-ttu-id="ac80e-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ac80e-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ac80e-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ac80e-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ac80e-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ac80e-114">Return code</span></span>                                                                          | <span data-ttu-id="ac80e-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac80e-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ac80e-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac80e-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ac80e-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac80e-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac80e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac80e-118">Remarks</span></span>

<span data-ttu-id="ac80e-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="ac80e-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="ac80e-120">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ac80e-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac80e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac80e-121">Requirements</span></span>



| <span data-ttu-id="ac80e-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac80e-122">Requirement</span></span> | <span data-ttu-id="ac80e-123">Wert</span><span class="sxs-lookup"><span data-stu-id="ac80e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac80e-124">Header</span><span class="sxs-lookup"><span data-stu-id="ac80e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ac80e-125"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac80e-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac80e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ac80e-126">Library</span></span><br/> | <dl> <span data-ttu-id="ac80e-127"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac80e-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac80e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac80e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac80e-129">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ac80e-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ac80e-130">**Iportablede vicevalues:: GetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="ac80e-130">**IPortableDeviceValues::GetBoolValue**</span></span>](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




