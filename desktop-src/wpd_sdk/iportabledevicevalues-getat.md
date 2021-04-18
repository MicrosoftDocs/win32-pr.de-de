---
description: Die GetAt-Methode ruft mit dem angegebenen Null basierten Index einen Wert aus der Auflistung ab.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Iportabledevicevalues:: GetAt-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365480"
---
# <a name="iportabledevicevaluesgetat-method"></a><span data-ttu-id="be9d1-103">Iportabledevicevalues:: GetAt-Methode</span><span class="sxs-lookup"><span data-stu-id="be9d1-103">IPortableDeviceValues::GetAt method</span></span>

<span data-ttu-id="be9d1-104">Die **GetAt** -Methode ruft mit dem angegebenen Null basierten Index einen Wert aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="be9d1-104">The **GetAt** method retrieves a value from the collection using the supplied zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be9d1-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="be9d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be9d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be9d1-107">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be9d1-107">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be9d1-108">Ein **DWORD** , das einen NULL basierten Index in der Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="be9d1-108">A **DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="be9d1-109">*pkey* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be9d1-109">*pKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be9d1-110">Ein optionaler **PropertyKey** -Zeiger, der den Schlüssel des angegebenen Elements abruft.</span><span class="sxs-lookup"><span data-stu-id="be9d1-110">An optional **PROPERTYKEY** pointer that retrieves the key of the specified item.</span></span>

</dd> <dt>

<span data-ttu-id="be9d1-111">*pValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be9d1-111">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be9d1-112">Ein optionaler **PROPVARIANT** , der den Wert des angegebenen Elements abruft.</span><span class="sxs-lookup"><span data-stu-id="be9d1-112">An optional **PROPVARIANT** that retrieves the value of the specified item.</span></span> <span data-ttu-id="be9d1-113">Der Aufrufer muss den Speicher freigeben, indem er **propvariantclear** aufruft, wenn er damit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="be9d1-113">The caller must free the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be9d1-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be9d1-114">Return value</span></span>

<span data-ttu-id="be9d1-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="be9d1-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="be9d1-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="be9d1-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="be9d1-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="be9d1-117">Return code</span></span>                                                                                  | <span data-ttu-id="be9d1-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be9d1-118">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="be9d1-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be9d1-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="be9d1-120">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be9d1-120">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="be9d1-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="be9d1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="be9d1-122">Es wurde eine ungültige Indexnummer angegeben.</span><span class="sxs-lookup"><span data-stu-id="be9d1-122">An invalid index number was specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="be9d1-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be9d1-123">Remarks</span></span>

<span data-ttu-id="be9d1-124">Wenn eine Eigenschaft einen Wert vom Typ VT \_ Unknown angibt, ist die Eigenschaft eines der tragbaren Windows-Geräte ([**iportabledevicekeycollection**](iportabledevicekeycollection.md), [**iportabledevicevaluescollection**](iportabledevicevaluescollection.md), [**iportabledevicevalues**](iportabledevicevalues.md) oder [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="be9d1-124">If a property indicates a value of type VT\_UNKNOWN, the property will be one of the Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) or [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span></span> <span data-ttu-id="be9d1-125">Von tragbaren Windows-Geräten können keine anderen Schnittstellen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be9d1-125">No other interfaces can be returned by Windows Portable Devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9d1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be9d1-126">Requirements</span></span>



| <span data-ttu-id="be9d1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be9d1-127">Requirement</span></span> | <span data-ttu-id="be9d1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="be9d1-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9d1-129">Header</span><span class="sxs-lookup"><span data-stu-id="be9d1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="be9d1-130"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="be9d1-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="be9d1-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be9d1-131">Library</span></span><br/> | <dl> <span data-ttu-id="be9d1-132"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be9d1-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9d1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be9d1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9d1-134">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="be9d1-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="be9d1-135">**Iportablede vicevalues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="be9d1-135">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




