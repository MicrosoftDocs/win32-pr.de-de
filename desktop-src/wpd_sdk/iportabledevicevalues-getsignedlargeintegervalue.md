---
description: Die getsignedlargeintegervalue-Methode ruft einen Longlong-Wert (Typ VT I8) ab, der \_ durch einen Schlüssel angegeben wird.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'Iportabledevicevalues:: getsignedlargeingetegervalue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355988"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a><span data-ttu-id="b21e5-103">Iportabledevicevalues:: getsignedlargeingetegervalue-Methode</span><span class="sxs-lookup"><span data-stu-id="b21e5-103">IPortableDeviceValues::GetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="b21e5-104">Die **getsignedlargeintegervalue** -Methode ruft einen **Longlong** -Wert (Typ VT I8) ab, der \_ durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b21e5-104">The **GetSignedLargeIntegerValue** method retrieves a **LONGLONG** value (type VT\_I8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b21e5-105">Syntax</span></span>


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b21e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b21e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b21e5-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b21e5-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21e5-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="b21e5-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b21e5-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b21e5-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b21e5-110">Zeiger auf den abgerufenen **ulong** -Wert.</span><span class="sxs-lookup"><span data-stu-id="b21e5-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b21e5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b21e5-111">Return value</span></span>

<span data-ttu-id="b21e5-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b21e5-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b21e5-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b21e5-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b21e5-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b21e5-114">Return code</span></span>                                                                                                            | <span data-ttu-id="b21e5-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b21e5-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b21e5-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b21e5-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="b21e5-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b21e5-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="b21e5-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="b21e5-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="b21e5-119">Die von *Key* angegebene Eigenschaft ist kein **Longlong** -Typ.</span><span class="sxs-lookup"><span data-stu-id="b21e5-119">The property specified by *key* is not a **LONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="b21e5-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="b21e5-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="b21e5-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b21e5-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="b21e5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b21e5-122">Requirements</span></span>



| <span data-ttu-id="b21e5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b21e5-123">Requirement</span></span> | <span data-ttu-id="b21e5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b21e5-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b21e5-125">Header</span><span class="sxs-lookup"><span data-stu-id="b21e5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b21e5-126"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b21e5-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b21e5-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b21e5-127">Library</span></span><br/> | <dl> <span data-ttu-id="b21e5-128"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b21e5-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b21e5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b21e5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21e5-130">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b21e5-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b21e5-131">**Iportablede vicevalues:: setsignedlargeingetegervalue**</span><span class="sxs-lookup"><span data-stu-id="b21e5-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




