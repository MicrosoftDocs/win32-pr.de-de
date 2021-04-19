---
description: Die getunsignedintegervalue-Methode ruft einen Ulong-Wert (Type VT UI4) ab, der \_ von einem Schlüssel angegeben wird.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'Iportabledevicevalues:: getunsignedintegervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373665"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a><span data-ttu-id="2f012-103">Iportabledevicevalues:: getunsignedintegervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="2f012-103">IPortableDeviceValues::GetUnsignedIntegerValue method</span></span>

<span data-ttu-id="2f012-104">Die **getunsignedintegervalue** -Methode ruft einen **ulong** -Wert (Type VT UI4) ab, der \_ von einem Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f012-104">The **GetUnsignedIntegerValue** method retrieves a **ULONG** value (type VT\_UI4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f012-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f012-105">Syntax</span></span>


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="2f012-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f012-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f012-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f012-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f012-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="2f012-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2f012-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2f012-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f012-110">Zeiger auf den abgerufenen **ulong** -Wert.</span><span class="sxs-lookup"><span data-stu-id="2f012-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f012-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f012-111">Return value</span></span>

<span data-ttu-id="2f012-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="2f012-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2f012-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2f012-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2f012-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2f012-114">Return code</span></span>                                                                                                            | <span data-ttu-id="2f012-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f012-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f012-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f012-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="2f012-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f012-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2f012-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="2f012-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="2f012-119">Die von *Key* angegebene Eigenschaft ist kein **ulong** -Typ.</span><span class="sxs-lookup"><span data-stu-id="2f012-119">The property specified by *key* is not a **ULONG** type.</span></span><br/>  |
| <dl> <span data-ttu-id="2f012-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="2f012-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="2f012-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="2f012-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="2f012-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f012-122">Examples</span></span>

<span data-ttu-id="2f012-123">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="2f012-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f012-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f012-124">Requirements</span></span>



| <span data-ttu-id="2f012-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f012-125">Requirement</span></span> | <span data-ttu-id="2f012-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2f012-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f012-127">Header</span><span class="sxs-lookup"><span data-stu-id="2f012-127">Header</span></span><br/>  | <dl> <span data-ttu-id="2f012-128"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f012-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f012-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f012-129">Library</span></span><br/> | <dl> <span data-ttu-id="2f012-130"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f012-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f012-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f012-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f012-132">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2f012-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2f012-133">**Iportableendvicevalues:: Server Value**</span><span class="sxs-lookup"><span data-stu-id="2f012-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span></span>](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="2f012-134">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2f012-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="2f012-135">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="2f012-135">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="2f012-136">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="2f012-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




