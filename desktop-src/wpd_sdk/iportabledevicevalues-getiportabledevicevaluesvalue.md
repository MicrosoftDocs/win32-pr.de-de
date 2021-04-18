---
description: Die getiportabledevicevaluesvalue-Methode ruft einen iportabledevicevalues-Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'Iportabledevicevalues:: getiportabledevicevaluesvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365773"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a><span data-ttu-id="c8ecf-103">Iportabledevicevalues:: getiportabledevicevaluesvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="c8ecf-103">IPortableDeviceValues::GetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="c8ecf-104">Die **getiportabledevicevaluesvalue** -Methode ruft einen **iportabledevicevalues** -Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-104">The **GetIPortableDeviceValuesValue** method retrieves an **IPortableDeviceValues** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ecf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8ecf-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="c8ecf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8ecf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ecf-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8ecf-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ecf-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c8ecf-109">*ppValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c8ecf-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ecf-110">Adresse einer Variablen, die einen Zeiger auf die [**abgerufene iportableendvicevalues**](iportabledevicevalues.md) -Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span> <span data-ttu-id="c8ecf-111">Der Aufrufer ist für das Aufrufen von **Release** an der abgerufenen Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8ecf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8ecf-112">Return value</span></span>

<span data-ttu-id="c8ecf-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c8ecf-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c8ecf-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c8ecf-115">Return code</span></span>                                                                                                            | <span data-ttu-id="c8ecf-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8ecf-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8ecf-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ecf-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="c8ecf-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-118">The method succeeded.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="c8ecf-119"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ecf-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="c8ecf-120">Die von *Key* angegebene Eigenschaft ist keine **iportabletovicevalues** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-120">The property specified by *key* is not an **IPortableDeviceValues** interface.</span></span><br/> |
| <dl> <span data-ttu-id="c8ecf-121"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="c8ecf-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="c8ecf-122">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c8ecf-122">The property specified by *key* is not in the collection.</span></span><br/>                      |



 

## <a name="examples"></a><span data-ttu-id="c8ecf-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8ecf-123">Examples</span></span>

<span data-ttu-id="c8ecf-124">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen unterstützter Dienst Ereignisse](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="c8ecf-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ecf-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8ecf-125">Requirements</span></span>



| <span data-ttu-id="c8ecf-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8ecf-126">Requirement</span></span> | <span data-ttu-id="c8ecf-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c8ecf-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ecf-128">Header</span><span class="sxs-lookup"><span data-stu-id="c8ecf-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c8ecf-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ecf-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8ecf-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c8ecf-130">Library</span></span><br/> | <dl> <span data-ttu-id="c8ecf-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8ecf-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ecf-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ecf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ecf-133">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c8ecf-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c8ecf-134">**Iportableendvicevalues:: endportableabvicevaluesvalue**</span><span class="sxs-lookup"><span data-stu-id="c8ecf-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[<span data-ttu-id="c8ecf-135">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c8ecf-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="c8ecf-136">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="c8ecf-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




