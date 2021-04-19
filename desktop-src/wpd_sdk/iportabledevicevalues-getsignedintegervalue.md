---
description: Die getsignedintegervalue-Methode ruft einen Long-Wert (Type VT I4) ab, der \_ von einem Schlüssel angegeben wird.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'Iportabledevicevalues:: getsignedintegervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2fe0c2f8714d3fa28f61624924eba169f9f1c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370920"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a><span data-ttu-id="7f9d4-103">Iportabledevicevalues:: getsignedintegervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="7f9d4-103">IPortableDeviceValues::GetSignedIntegerValue method</span></span>

<span data-ttu-id="7f9d4-104">Die **getsignedintegervalue** -Methode ruft einen **Long** -Wert (Type VT I4) ab, der \_ von einem Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-104">The **GetSignedIntegerValue** method retrieves a **LONG** value (type VT\_I4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9d4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f9d4-105">Syntax</span></span>


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="7f9d4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f9d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f9d4-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f9d4-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9d4-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7f9d4-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7f9d4-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9d4-110">Zeiger auf den abgerufenen **Long** -Wert.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-110">Pointer to the retrieved **LONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f9d4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f9d4-111">Return value</span></span>

<span data-ttu-id="7f9d4-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7f9d4-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7f9d4-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7f9d4-114">Return code</span></span>                                                                                                            | <span data-ttu-id="7f9d4-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f9d4-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f9d4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d4-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="7f9d4-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="7f9d4-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d4-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="7f9d4-119">Die von *Key* angegebene Eigenschaft ist kein **Long** -Typ.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-119">The property specified by *key* is not a **LONG** type.</span></span><br/>   |
| <dl> <span data-ttu-id="7f9d4-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d4-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="7f9d4-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="7f9d4-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f9d4-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f9d4-122">Requirements</span></span>



| <span data-ttu-id="7f9d4-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f9d4-123">Requirement</span></span> | <span data-ttu-id="7f9d4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="7f9d4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9d4-125">Header</span><span class="sxs-lookup"><span data-stu-id="7f9d4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7f9d4-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d4-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f9d4-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f9d4-127">Library</span></span><br/> | <dl> <span data-ttu-id="7f9d4-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f9d4-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f9d4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f9d4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9d4-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7f9d4-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="7f9d4-131">**Iportabledebug:: setsignedintegervalue**</span><span class="sxs-lookup"><span data-stu-id="7f9d4-131">**IPortableDeviceValues::SetSignedIntegerValue**</span></span>](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




