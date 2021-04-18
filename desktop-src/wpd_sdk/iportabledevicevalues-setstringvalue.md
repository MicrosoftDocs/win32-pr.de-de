---
description: Die SetStringValue-Methode fügt einen neuen Zeichen folgen Wert (Type VT \_ LPWSTR) hinzu oder überschreibt eine vorhandene.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'Iportabledevicevalues:: SetStringValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366017"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a><span data-ttu-id="e072a-103">Iportabledevicevalues:: SetStringValue-Methode</span><span class="sxs-lookup"><span data-stu-id="e072a-103">IPortableDeviceValues::SetStringValue method</span></span>

<span data-ttu-id="e072a-104">Die **SetStringValue** -Methode fügt einen neuen Zeichen folgen Wert (Type VT \_ LPWSTR) hinzu oder überschreibt eine vorhandene.</span><span class="sxs-lookup"><span data-stu-id="e072a-104">The **SetStringValue** method adds a new string value (type VT\_LPWSTR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e072a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e072a-105">Syntax</span></span>


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a><span data-ttu-id="e072a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e072a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e072a-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e072a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e072a-108">Ein **refpropertykey** , der das Element angibt, das erstellt oder überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="e072a-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="e072a-109">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e072a-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e072a-110">Ein **LPCWSTR** , der den neuen Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="e072a-110">A **LPCWSTR** that specifies the new value.</span></span> <span data-ttu-id="e072a-111">Die Zeichenfolge wird kopiert, sodass der Aufrufer den für diesen Wert zugeordneten Arbeitsspeicher nach dem Aufrufen dieser Methode freigeben kann.</span><span class="sxs-lookup"><span data-stu-id="e072a-111">The string is copied, so the caller can release the memory allocated for this value after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e072a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e072a-112">Return value</span></span>

<span data-ttu-id="e072a-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="e072a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e072a-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e072a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e072a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e072a-115">Return code</span></span>                                                                          | <span data-ttu-id="e072a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e072a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e072a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e072a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e072a-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e072a-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e072a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e072a-119">Remarks</span></span>

<span data-ttu-id="e072a-120">Der vorhandene Schlüsselspeicher wird entsprechend freigegeben.</span><span class="sxs-lookup"><span data-stu-id="e072a-120">Any existing key memory will be released appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="e072a-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e072a-121">Examples</span></span>

<span data-ttu-id="e072a-122">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Angeben von Client Informationen](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="e072a-122">For an example of how to use this method, see [Specifying Client Information](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e072a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e072a-123">Requirements</span></span>



| <span data-ttu-id="e072a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e072a-124">Requirement</span></span> | <span data-ttu-id="e072a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e072a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e072a-126">Header</span><span class="sxs-lookup"><span data-stu-id="e072a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e072a-127"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e072a-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e072a-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e072a-128">Library</span></span><br/> | <dl> <span data-ttu-id="e072a-129"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e072a-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e072a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e072a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e072a-131">Hinzufügen einer Ressource zu einem Objekt</span><span class="sxs-lookup"><span data-stu-id="e072a-131">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="e072a-132">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e072a-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e072a-133">**Iportablede vicevalues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="e072a-133">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[<span data-ttu-id="e072a-134">Festlegen von Eigenschaften für ein einzelnes Objekt</span><span class="sxs-lookup"><span data-stu-id="e072a-134">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="e072a-135">Festlegen von Eigenschaften für mehrere Objekte</span><span class="sxs-lookup"><span data-stu-id="e072a-135">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> <dt>

[<span data-ttu-id="e072a-136">Angeben von Client Informationen</span><span class="sxs-lookup"><span data-stu-id="e072a-136">Specifying Client Information</span></span>](specifying-client-information.md)
</dt> <dt>

[<span data-ttu-id="e072a-137">Schreiben von Content-Object-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e072a-137">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




