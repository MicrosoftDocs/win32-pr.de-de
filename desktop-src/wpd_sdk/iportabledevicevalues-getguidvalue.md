---
description: Die getguidvalue-Methode ruft einen GUID-Wert (Type VT \_ CLSID) ab, der von einem Schlüssel angegeben wird.
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'Iportabledevicevalues:: getguidvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 362672daad835a2e843edeaf6dc517884c25f1ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358731"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a><span data-ttu-id="be462-103">Iportabledevicevalues:: getguidvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="be462-103">IPortableDeviceValues::GetGuidValue method</span></span>

<span data-ttu-id="be462-104">Die **getguidvalue** -Methode ruft einen **GUID** -Wert (Type VT \_ CLSID) ab, der von einem Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="be462-104">The **GetGuidValue** method retrieves a **GUID** value (type VT\_CLSID) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="be462-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be462-105">Syntax</span></span>


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="be462-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be462-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be462-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be462-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be462-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="be462-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="be462-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="be462-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be462-110">Zeiger auf den abgerufenen **GUID** -Wert.</span><span class="sxs-lookup"><span data-stu-id="be462-110">Pointer to the retrieved **GUID** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be462-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be462-111">Return value</span></span>

<span data-ttu-id="be462-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="be462-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="be462-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="be462-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="be462-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="be462-114">Return code</span></span>                                                                                                            | <span data-ttu-id="be462-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be462-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="be462-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be462-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="be462-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be462-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="be462-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="be462-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="be462-119">Die von *Key* angegebene Eigenschaft ist kein **GUID** -Typ.</span><span class="sxs-lookup"><span data-stu-id="be462-119">The property specified by *key* is not a **GUID** type.</span></span><br/>   |
| <dl> <span data-ttu-id="be462-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="be462-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="be462-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="be462-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="be462-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be462-122">Examples</span></span>

<span data-ttu-id="be462-123">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Methoden](retrieving-supported-methods.md).</span><span class="sxs-lookup"><span data-stu-id="be462-123">For an example of how to use this method, see [Retrieving Supported Service Methods](retrieving-supported-methods.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be462-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be462-124">Requirements</span></span>



| <span data-ttu-id="be462-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be462-125">Requirement</span></span> | <span data-ttu-id="be462-126">Wert</span><span class="sxs-lookup"><span data-stu-id="be462-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be462-127">Header</span><span class="sxs-lookup"><span data-stu-id="be462-127">Header</span></span><br/>  | <dl> <span data-ttu-id="be462-128"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="be462-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="be462-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be462-129">Library</span></span><br/> | <dl> <span data-ttu-id="be462-130"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be462-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be462-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be462-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be462-132">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="be462-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="be462-133">**Iportabledebug:: setguidvalue**</span><span class="sxs-lookup"><span data-stu-id="be462-133">**IPortableDeviceValues::SetGuidValue**</span></span>](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[<span data-ttu-id="be462-134">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="be462-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="be462-135">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="be462-135">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




