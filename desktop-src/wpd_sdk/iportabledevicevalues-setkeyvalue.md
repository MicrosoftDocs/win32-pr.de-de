---
description: Die SetKeyValue-Methode fügt einen neuen Ref PropertyKey-Wert hinzu (Typ VT \_ unknown) oder überschreibt eine vorhandene.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'Iportabledevicevalues:: SetKeyValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351276"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a><span data-ttu-id="38459-103">Iportabledevicevalues:: SetKeyValue-Methode</span><span class="sxs-lookup"><span data-stu-id="38459-103">IPortableDeviceValues::SetKeyValue method</span></span>

<span data-ttu-id="38459-104">Die **SetKeyValue** -Methode fügt einen neuen **ref PropertyKey** -Wert hinzu (Typ VT \_ unknown) oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="38459-104">The **SetKeyValue** method adds a new **REFPROPERTYKEY** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="38459-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38459-105">Syntax</span></span>


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a><span data-ttu-id="38459-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38459-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38459-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38459-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38459-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="38459-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="38459-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38459-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38459-110">Ein **ref PropertyKey** , der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="38459-110">A **REFPROPERTYKEY** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38459-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38459-111">Return value</span></span>

<span data-ttu-id="38459-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="38459-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="38459-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="38459-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="38459-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="38459-114">Return code</span></span>                                                                          | <span data-ttu-id="38459-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38459-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="38459-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38459-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="38459-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38459-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="38459-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38459-118">Remarks</span></span>

<span data-ttu-id="38459-119">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="38459-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="38459-120">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="38459-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="38459-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38459-121">Requirements</span></span>



| <span data-ttu-id="38459-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38459-122">Requirement</span></span> | <span data-ttu-id="38459-123">Wert</span><span class="sxs-lookup"><span data-stu-id="38459-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38459-124">Header</span><span class="sxs-lookup"><span data-stu-id="38459-124">Header</span></span><br/>  | <dl> <span data-ttu-id="38459-125"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="38459-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="38459-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38459-126">Library</span></span><br/> | <dl> <span data-ttu-id="38459-127"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38459-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38459-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38459-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38459-129">Hinzufügen einer Ressource zu einem Objekt</span><span class="sxs-lookup"><span data-stu-id="38459-129">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="38459-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="38459-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="38459-131">**Iportablede vicevalues:: getkeyvalue**</span><span class="sxs-lookup"><span data-stu-id="38459-131">**IPortableDeviceValues::GetKeyValue**</span></span>](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




