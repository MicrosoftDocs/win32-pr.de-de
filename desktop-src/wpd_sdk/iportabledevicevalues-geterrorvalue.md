---
description: Die geterrorvalue-Methode ruft einen HRESULT-Wert (Type VT Error) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: af57ddbd-5503-4b9b-bd75-ba9c9c202b73
title: 'Iportabledevicevalues:: geterrorvalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 86e5dacfa398cfe2bb57bfd289e4c8e792f14a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356486"
---
# <a name="iportabledevicevaluesgeterrorvalue-method"></a><span data-ttu-id="aec71-103">Iportabledevicevalues:: geterrorvalue-Methode</span><span class="sxs-lookup"><span data-stu-id="aec71-103">IPortableDeviceValues::GetErrorValue method</span></span>

<span data-ttu-id="aec71-104">Die **geterrorvalue** -Methode ruft einen **HRESULT** -Wert (Type VT Error) ab, der \_ durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aec71-104">The **GetErrorValue** method retrieves an **HRESULT** value (type VT\_ERROR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="aec71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aec71-105">Syntax</span></span>


```C++
HRESULT GetErrorValue(
  [in]  REFPROPERTYKEY key,
  [out] HRESULT        *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="aec71-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aec71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aec71-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aec71-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aec71-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="aec71-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="aec71-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aec71-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aec71-110">Zeiger auf den abgerufenen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="aec71-110">Pointer to the retrieved **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aec71-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aec71-111">Return value</span></span>

<span data-ttu-id="aec71-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="aec71-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aec71-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="aec71-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aec71-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="aec71-114">Return code</span></span>                                                                                                            | <span data-ttu-id="aec71-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aec71-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aec71-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aec71-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="aec71-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aec71-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="aec71-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="aec71-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="aec71-119">Die von *Key* angegebene Eigenschaft ist kein **HRESULT** -Typ.</span><span class="sxs-lookup"><span data-stu-id="aec71-119">The property specified by *key* is not an **HRESULT** type.</span></span><br/> |
| <dl> <span data-ttu-id="aec71-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="aec71-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="aec71-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="aec71-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="aec71-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec71-122">Requirements</span></span>



| <span data-ttu-id="aec71-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aec71-123">Requirement</span></span> | <span data-ttu-id="aec71-124">Wert</span><span class="sxs-lookup"><span data-stu-id="aec71-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aec71-125">Header</span><span class="sxs-lookup"><span data-stu-id="aec71-125">Header</span></span><br/>  | <dl> <span data-ttu-id="aec71-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec71-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="aec71-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aec71-127">Library</span></span><br/> | <dl> <span data-ttu-id="aec71-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aec71-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aec71-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aec71-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aec71-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="aec71-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="aec71-131">**Iportablede vicevalues:: Server-Wert**</span><span class="sxs-lookup"><span data-stu-id="aec71-131">**IPortableDeviceValues::SetErrorValue**</span></span>](iportabledevicevalues-seterrorvalue.md)
</dt> </dl>

 

 




