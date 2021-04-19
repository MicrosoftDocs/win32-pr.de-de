---
description: Die getiportabledevicepropvariantcollectionvalue-Methode ruft einen iportabledevicepropvariantcollection-Wert (Typ VT \_ unknown) ab, der durch einen Schlüssel angegeben wird.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'Iportabledevicevalues:: getiportabledevicepropvariantcollectionvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372465"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="6c4c8-103">Iportabledevicevalues:: getiportabledevicepropvariantcollectionvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="6c4c8-103">IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="6c4c8-104">Die **getiportabledevicepropvariantcollectionvalue** -Methode ruft einen **iportabledevicepropvariantcollection** -Wert (Typ VT \_ unknown) ab, der durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-104">The **GetIPortableDevicePropVariantCollectionValue** method retrieves an **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c4c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c4c8-105">Syntax</span></span>


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="6c4c8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c4c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4c8-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c4c8-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4c8-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6c4c8-109">*ppValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c4c8-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c4c8-110">Adresse einer Variablen, die einen Zeiger auf die abgerufene [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-110">Address of a variable that receives a pointer to the retrieved [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface.</span></span> <span data-ttu-id="6c4c8-111">Der Aufrufer ist für das Aufrufen von **Release** an der abgerufenen Schnittstelle verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c4c8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c4c8-112">Return value</span></span>

<span data-ttu-id="6c4c8-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6c4c8-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6c4c8-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6c4c8-115">Return code</span></span>                                                                                                            | <span data-ttu-id="6c4c8-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c4c8-116">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c4c8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c8-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="6c4c8-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-118">The method succeeded.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="6c4c8-119"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c8-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="6c4c8-120">Die von *Key* angegebene Eigenschaft ist keine **iportabledevicepropvariantcollection** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-120">The property specified by *key* is not an **IPortableDevicePropVariantCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="6c4c8-121"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c8-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="6c4c8-122">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6c4c8-122">The property specified by *key* is not in the collection.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="6c4c8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c4c8-123">Requirements</span></span>



| <span data-ttu-id="6c4c8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c4c8-124">Requirement</span></span> | <span data-ttu-id="6c4c8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6c4c8-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4c8-126">Header</span><span class="sxs-lookup"><span data-stu-id="6c4c8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6c4c8-127"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c8-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c4c8-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c4c8-128">Library</span></span><br/> | <dl> <span data-ttu-id="6c4c8-129"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c4c8-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4c8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c4c8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4c8-131">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="6c4c8-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="6c4c8-132">**Iportableendvicevalues:: "endportabledevicepropvariantcollectionvalue"**</span><span class="sxs-lookup"><span data-stu-id="6c4c8-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




