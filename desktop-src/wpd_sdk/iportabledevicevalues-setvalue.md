---
description: Die SetValue-Methode fügt einen neuen PROPVARIANT-Wert hinzu oder überschreibt eine vorhandene.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'Iportabledevicevalues:: SetValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370642"
---
# <a name="iportabledevicevaluessetvalue-method"></a><span data-ttu-id="b7d8c-103">Iportabledevicevalues:: SetValue-Methode</span><span class="sxs-lookup"><span data-stu-id="b7d8c-103">IPortableDeviceValues::SetValue method</span></span>

<span data-ttu-id="b7d8c-104">Die **SetValue** -Methode fügt einen neuen **PROPVARIANT** -Wert hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-104">The **SetValue** method adds a new **PROPVARIANT** value or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7d8c-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b7d8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7d8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d8c-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7d8c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d8c-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="b7d8c-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7d8c-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7d8c-110">Ein **PROPVARIANT** -Wert, der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-110">A **PROPVARIANT** that specifies the new value.</span></span> <span data-ttu-id="b7d8c-111">Das SDK kopiert den Wert, sodass der Aufrufer die lokale Variable durch Aufrufen von **propvariantclear** freigeben kann, nachdem diese Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-111">The SDK copies the value, so the caller can release the local variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d8c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7d8c-112">Return value</span></span>

<span data-ttu-id="b7d8c-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b7d8c-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b7d8c-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b7d8c-115">Return code</span></span>                                                                          | <span data-ttu-id="b7d8c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7d8c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b7d8c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b7d8c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b7d8c-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7d8c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7d8c-119">Remarks</span></span>

<span data-ttu-id="b7d8c-120">Wenn VarType für *pValue den Wert* VT \_ Vector oder VT \_ UI1 aufweist, wird das Festlegen eines Puffers, **der NULL** oder NULL ist, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-120">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="b7d8c-121">Beispielsweise sind weder pValue. Caub. pelems = **null** noch pValue. Caub. celems = 0 zulässig.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-121">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="b7d8c-122">Diese Methode kann verwendet werden, um einen Wert eines beliebigen Typs aus der Auflistung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-122">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="b7d8c-123">Wenn Sie jedoch den Werttyp im Voraus kennen, verwenden Sie eine der spezialisierten **Set...** -Methoden dieser Schnittstelle, um den mehr Aufwand bei der direkten Arbeit mit PROPVARIANT-Werten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-123">However, if you know the value type in advance, use one of the specialized **Set...** methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

<span data-ttu-id="b7d8c-124">Wenn ein vorhandener Wert über denselben Schlüssel verfügt, der durch den *Schlüssel* Parameter angegeben wird, wird der vorhandene Wert ohne Warnung überschrieben.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-124">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="b7d8c-125">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="b7d8c-125">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d8c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7d8c-126">Requirements</span></span>



| <span data-ttu-id="b7d8c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7d8c-127">Requirement</span></span> | <span data-ttu-id="b7d8c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d8c-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d8c-129">Header</span><span class="sxs-lookup"><span data-stu-id="b7d8c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b7d8c-130"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d8c-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7d8c-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b7d8c-131">Library</span></span><br/> | <dl> <span data-ttu-id="b7d8c-132"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7d8c-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d8c-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d8c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d8c-134">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b7d8c-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b7d8c-135">**Iportablede vicevalues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="b7d8c-135">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="b7d8c-136">**Iportablede vicevalues:: removeValue**</span><span class="sxs-lookup"><span data-stu-id="b7d8c-136">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




