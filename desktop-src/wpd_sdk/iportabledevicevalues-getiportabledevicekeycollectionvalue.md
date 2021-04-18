---
description: Die getiportabledevicekeycollectionvalue-Methode ruft einen iportabledevicekeycollection-Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'Iportabledevicevalues:: getiportabledevicekeycollectionvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364965"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="a8f94-103">Iportabledevicevalues:: getiportabledevicekeycollectionvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="a8f94-103">IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="a8f94-104">Die **getiportabledevicekeycollectionvalue** -Methode ruft einen **iportabledevicekeycollection** -Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a8f94-104">The **GetIPortableDeviceKeyCollectionValue** method retrieves an **IPortableDeviceKeyCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f94-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8f94-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="a8f94-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f94-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8f94-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f94-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="a8f94-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a8f94-109">*ppValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a8f94-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f94-110">Zeiger auf den abgerufenen [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="a8f94-110">Pointer to the retrieved [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface pointer.</span></span> <span data-ttu-id="a8f94-111">Der Aufrufer ist für das Aufrufen von **Release** an der abgerufenen Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="a8f94-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f94-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8f94-112">Return value</span></span>

<span data-ttu-id="a8f94-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a8f94-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a8f94-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a8f94-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a8f94-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a8f94-115">Return code</span></span>                                                                                                            | <span data-ttu-id="a8f94-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8f94-116">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8f94-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a8f94-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="a8f94-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a8f94-118">The method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="a8f94-119"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="a8f94-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="a8f94-120">Die von *Key* angegebene Eigenschaft ist keine **iportabledevicekeycollection** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a8f94-120">The property specified by *key* is not an **IPortableDeviceKeyCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="a8f94-121"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="a8f94-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="a8f94-122">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="a8f94-122">The property specified by *key* is not in the collection.</span></span><br/>                             |



 

## <a name="examples"></a><span data-ttu-id="a8f94-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8f94-123">Examples</span></span>

<span data-ttu-id="a8f94-124">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="a8f94-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f94-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8f94-125">Requirements</span></span>



| <span data-ttu-id="a8f94-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8f94-126">Requirement</span></span> | <span data-ttu-id="a8f94-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a8f94-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f94-128">Header</span><span class="sxs-lookup"><span data-stu-id="a8f94-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a8f94-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f94-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8f94-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8f94-130">Library</span></span><br/> | <dl> <span data-ttu-id="a8f94-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8f94-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f94-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8f94-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f94-133">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a8f94-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a8f94-134">**Iportableendvicevalues:: Server Type Report abledevicekeycollectionvalue**</span><span class="sxs-lookup"><span data-stu-id="a8f94-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[<span data-ttu-id="a8f94-135">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a8f94-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="a8f94-136">Abrufen unterstützter Dienst Methoden</span><span class="sxs-lookup"><span data-stu-id="a8f94-136">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




