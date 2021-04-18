---
description: Die getiunknownvalue-Methode ruft einen IUnknown-Schnittstellen Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'Iportabledevicevalues:: getiunknownvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365423"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a><span data-ttu-id="b44cb-103">Iportabledevicevalues:: getiunknownvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="b44cb-103">IPortableDeviceValues::GetIUnknownValue method</span></span>

<span data-ttu-id="b44cb-104">Die **getiunknownvalue** -Methode ruft einen **IUnknown** -Schnittstellen Wert (Typ VT unknown) ab, der \_ durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b44cb-104">The **GetIUnknownValue** method retrieves an **IUnknown** interface value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b44cb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b44cb-105">Syntax</span></span>


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="b44cb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b44cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b44cb-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b44cb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b44cb-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="b44cb-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b44cb-109">*ppValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b44cb-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b44cb-110">Adresse einer Variablen, die einen Zeiger auf die abgerufene **IUnknown** -Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="b44cb-110">Address of a variable that receives a pointer to the retrieved **IUnknown** interface.</span></span> <span data-ttu-id="b44cb-111">Der Aufrufer ist für das Aufrufen von **Release** an der abgerufenen Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="b44cb-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b44cb-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b44cb-112">Return value</span></span>

<span data-ttu-id="b44cb-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b44cb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b44cb-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b44cb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b44cb-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b44cb-115">Return code</span></span>                                                                                                            | <span data-ttu-id="b44cb-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b44cb-116">Description</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b44cb-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b44cb-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="b44cb-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b44cb-118">The method succeeded.</span></span><br/>                                             |
| <dl> <span data-ttu-id="b44cb-119"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="b44cb-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="b44cb-120">Die von *Key* angegebene Eigenschaft ist keine **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b44cb-120">The property specified by *key* is not an **IUnknown** interface.</span></span><br/> |
| <dl> <span data-ttu-id="b44cb-121"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="b44cb-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="b44cb-122">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b44cb-122">The property specified by *key* is not in the collection.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="b44cb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b44cb-123">Requirements</span></span>



| <span data-ttu-id="b44cb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b44cb-124">Requirement</span></span> | <span data-ttu-id="b44cb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b44cb-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b44cb-126">Header</span><span class="sxs-lookup"><span data-stu-id="b44cb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b44cb-127"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b44cb-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b44cb-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b44cb-128">Library</span></span><br/> | <dl> <span data-ttu-id="b44cb-129"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b44cb-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b44cb-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b44cb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44cb-131">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b44cb-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b44cb-132">**Iportablede vicevalues:: Server Wert**</span><span class="sxs-lookup"><span data-stu-id="b44cb-132">**IPortableDeviceValues::SetIUnknownValue**</span></span>](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




