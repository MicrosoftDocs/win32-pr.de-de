---
description: Die getunsignedlargeintegervalue-Methode ruft einen ULONGLONG-Wert (Typ VT UI8) ab, der \_ von einem Schlüssel angegeben wird.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'Iportabledevicevalues:: getunsignedlargeingetegervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358289"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a><span data-ttu-id="d1924-103">Iportabledevicevalues:: getunsignedlargeingetegervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="d1924-103">IPortableDeviceValues::GetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="d1924-104">Die **getunsignedlargeintegervalue** -Methode ruft einen **ULONGLONG** -Wert (Typ VT UI8) ab, der \_ von einem Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d1924-104">The **GetUnsignedLargeIntegerValue** method retrieves a **ULONGLONG** value (type VT\_UI8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1924-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1924-105">Syntax</span></span>


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="d1924-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1924-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1924-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d1924-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1924-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="d1924-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d1924-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d1924-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1924-110">Zeiger auf den abgerufenen **ULONGLONG** -Wert.</span><span class="sxs-lookup"><span data-stu-id="d1924-110">Pointer to the retrieved **ULONGLONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1924-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1924-111">Return value</span></span>

<span data-ttu-id="d1924-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="d1924-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d1924-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1924-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d1924-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d1924-114">Return code</span></span>                                                                                                            | <span data-ttu-id="d1924-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1924-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1924-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1924-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="d1924-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1924-117">The method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="d1924-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="d1924-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="d1924-119">Die von *Key* angegebene Eigenschaft ist kein **ULONGLONG** -Typ.</span><span class="sxs-lookup"><span data-stu-id="d1924-119">The property specified by *key* is not a **ULONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="d1924-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="d1924-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="d1924-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="d1924-121">The property specified by *key* is not in the collection.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="d1924-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1924-122">Requirements</span></span>



| <span data-ttu-id="d1924-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1924-123">Requirement</span></span> | <span data-ttu-id="d1924-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d1924-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1924-125">Header</span><span class="sxs-lookup"><span data-stu-id="d1924-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d1924-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1924-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1924-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1924-127">Library</span></span><br/> | <dl> <span data-ttu-id="d1924-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1924-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1924-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1924-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1924-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="d1924-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d1924-131">**Iportableendvicevalues:: Abbild-ID-Wert**</span><span class="sxs-lookup"><span data-stu-id="d1924-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




