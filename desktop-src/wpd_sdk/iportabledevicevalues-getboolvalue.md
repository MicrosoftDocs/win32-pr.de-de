---
description: Die GetBoolValue-Methode ruft einen booleschen Wert (Typ VT \_ bool) ab, der durch einen Schlüssel angegeben wird.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'Iportabledevicevalues:: GetBoolValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358350"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a><span data-ttu-id="c0f27-103">Iportabledevicevalues:: GetBoolValue-Methode</span><span class="sxs-lookup"><span data-stu-id="c0f27-103">IPortableDeviceValues::GetBoolValue method</span></span>

<span data-ttu-id="c0f27-104">Die **GetBoolValue** -Methode ruft einen **booleschen** Wert (Typ VT \_ bool) ab, der durch einen Schlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c0f27-104">The **GetBoolValue** method retrieves a **Boolean** value (type VT\_BOOL) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0f27-105">Syntax</span></span>


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="c0f27-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0f27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f27-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0f27-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f27-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="c0f27-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c0f27-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c0f27-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f27-110">Zeiger auf den abgerufenen **booleschen** Wert.</span><span class="sxs-lookup"><span data-stu-id="c0f27-110">Pointer to the retrieved **BOOL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f27-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0f27-111">Return value</span></span>

<span data-ttu-id="c0f27-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c0f27-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c0f27-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c0f27-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c0f27-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c0f27-114">Return code</span></span>                                                                                                            | <span data-ttu-id="c0f27-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0f27-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0f27-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f27-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="c0f27-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0f27-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="c0f27-118"><dt>**DISP \_ E \_ typemismatch**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f27-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="c0f27-119">Die von *Key* angegebene Eigenschaft ist kein **boolescher** Typ.</span><span class="sxs-lookup"><span data-stu-id="c0f27-119">The property specified by *key* is not a **BOOL** type.</span></span><br/>   |
| <dl> <span data-ttu-id="c0f27-120"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f27-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="c0f27-121">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="c0f27-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="c0f27-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0f27-122">Examples</span></span>

<span data-ttu-id="c0f27-123">Ein Beispiel für die Verwendung dieser Methode finden Sie unter [Festlegen von Eigenschaften für ein einzelnes Objekt](setting-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="c0f27-123">For an example of how to use this method, see [Setting Properties for a Single Object](setting-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f27-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0f27-124">Requirements</span></span>



| <span data-ttu-id="c0f27-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0f27-125">Requirement</span></span> | <span data-ttu-id="c0f27-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c0f27-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f27-127">Header</span><span class="sxs-lookup"><span data-stu-id="c0f27-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c0f27-128"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f27-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0f27-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0f27-129">Library</span></span><br/> | <dl> <span data-ttu-id="c0f27-130"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0f27-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f27-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0f27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f27-132">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c0f27-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c0f27-133">**Iportabledebug:: SetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="c0f27-133">**IPortableDeviceValues::SetBoolValue**</span></span>](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[<span data-ttu-id="c0f27-134">Abrufen unterstützter Dienst Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c0f27-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="c0f27-135">Festlegen von Eigenschaften für ein einzelnes Objekt</span><span class="sxs-lookup"><span data-stu-id="c0f27-135">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="c0f27-136">Schreiben von Content-Object-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c0f27-136">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




