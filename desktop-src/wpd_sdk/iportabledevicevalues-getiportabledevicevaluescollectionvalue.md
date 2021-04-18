---
description: Die getiportabledevicevaluescollectionvalue-Methode ruft einen iportabledevicevaluescollection-Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'Iportabledevicevalues:: getiportabledevicevaluescollectionvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358038"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="2817e-103">Iportabledevicevalues:: getiportabledevicevaluescollectionvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="2817e-103">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="2817e-104">Die **getiportabledevicevaluescollectionvalue** -Methode ruft einen **iportabledevicevaluescollection** -Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2817e-104">The **GetIPortableDeviceValuesCollectionValue** method retrieves an **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2817e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2817e-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="2817e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2817e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2817e-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2817e-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2817e-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="2817e-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2817e-109">*ppValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2817e-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2817e-110">Adresse einer Variablen, die einen Zeiger auf die [**abgerufene iportableendvicevaluescollection**](iportabledevicevaluescollection.md) -Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="2817e-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) interface.</span></span> <span data-ttu-id="2817e-111">Der Aufrufer ist für das Aufrufen von **Release** an der abgerufenen Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="2817e-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2817e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2817e-112">Return value</span></span>

<span data-ttu-id="2817e-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="2817e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2817e-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2817e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2817e-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2817e-115">Return code</span></span>                                                                                                            | <span data-ttu-id="2817e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2817e-116">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2817e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2817e-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="2817e-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2817e-118">The method succeeded.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="2817e-119"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="2817e-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="2817e-120">Die von *Key* angegebene Eigenschaft ist keine **iportabletovicevaluescollection** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2817e-120">The property specified by *key* is not an **IPortableDeviceValuesCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="2817e-121"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="2817e-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="2817e-122">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="2817e-122">The property specified by *key* is not in the collection.</span></span><br/>                                |



 

## <a name="examples"></a><span data-ttu-id="2817e-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2817e-123">Examples</span></span>

<span data-ttu-id="2817e-124">Ein Beispiel für die Verwendung dieser Methode finden Sie [unter Abrufen der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="2817e-124">For an example of how to use this method, see [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2817e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2817e-125">Requirements</span></span>



| <span data-ttu-id="2817e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2817e-126">Requirement</span></span> | <span data-ttu-id="2817e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2817e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2817e-128">Header</span><span class="sxs-lookup"><span data-stu-id="2817e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2817e-129"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="2817e-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="2817e-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2817e-130">Library</span></span><br/> | <dl> <span data-ttu-id="2817e-131"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2817e-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2817e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2817e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2817e-133">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2817e-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="2817e-134">Abrufen der von einem Gerät unterstützten Renderingfunktionen</span><span class="sxs-lookup"><span data-stu-id="2817e-134">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="2817e-135">**"Stiportableendvicevaluescollectionvalue"**</span><span class="sxs-lookup"><span data-stu-id="2817e-135">**SetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




