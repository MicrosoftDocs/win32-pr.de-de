---
description: Die GetValue-Methode ruft einen durch einen Schlüssel angegebenen PROPVARIANT-Wert ab.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'Iportabledevicevalues:: GetValue-Methode (portabledevicetypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352885"
---
# <a name="iportabledevicevaluesgetvalue-method"></a><span data-ttu-id="35b3f-103">Iportabledevicevalues:: GetValue-Methode</span><span class="sxs-lookup"><span data-stu-id="35b3f-103">IPortableDeviceValues::GetValue method</span></span>

<span data-ttu-id="35b3f-104">Die **GetValue** -Methode ruft einen durch einen Schlüssel angegebenen **PROPVARIANT** -Wert ab.</span><span class="sxs-lookup"><span data-stu-id="35b3f-104">The **GetValue** method retrieves a **PROPVARIANT** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="35b3f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35b3f-105">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="35b3f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35b3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35b3f-107">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35b3f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35b3f-108">Ein **refpropertykey** -Schlüssel, der das abzurufende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="35b3f-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="35b3f-109">*pValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="35b3f-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35b3f-110">Zeiger auf den abgerufenen **PROPVARIANT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="35b3f-110">Pointer to the retrieved **PROPVARIANT** value.</span></span> <span data-ttu-id="35b3f-111">Der Aufrufer muss den Speicher freigeben, indem er **propvariantclear** aufruft, wenn er damit abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="35b3f-111">The caller must release the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35b3f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35b3f-112">Return value</span></span>

<span data-ttu-id="35b3f-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="35b3f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="35b3f-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="35b3f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="35b3f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="35b3f-115">Return code</span></span>                                                                                                            | <span data-ttu-id="35b3f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35b3f-116">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="35b3f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="35b3f-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="35b3f-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35b3f-118">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="35b3f-119"><dt>**HRESULT \_ von \_ Win32 (Fehler \_ nicht \_ gefunden)**</dt></span><span class="sxs-lookup"><span data-stu-id="35b3f-119"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="35b3f-120">Die von *Key* angegebene Eigenschaft ist nicht in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="35b3f-120">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35b3f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35b3f-121">Remarks</span></span>

<span data-ttu-id="35b3f-122">Wenn VarType für *pValue den Wert* VT \_ Vector oder VT \_ UI1 aufweist, wird das  Abrufen eines Puffers mit der Größe Null oder der Größe 0 (null) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35b3f-122">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="35b3f-123">Beispielsweise sind weder pValue. Caub. pelems = **null** noch pValue. Caub. celems = 0 zulässig.</span><span class="sxs-lookup"><span data-stu-id="35b3f-123">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="35b3f-124">Diese Methode kann verwendet werden, um einen Wert eines beliebigen Typs aus der Auflistung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="35b3f-124">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="35b3f-125">Wenn Sie jedoch den Werttyp im Voraus kennen, verwenden Sie eine der spezialisierten Abruf Methoden dieser Schnittstelle, um den mehr Aufwand bei der direkten Arbeit mit PROPVARIANT-Werten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="35b3f-125">However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="35b3f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35b3f-126">Requirements</span></span>



| <span data-ttu-id="35b3f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35b3f-127">Requirement</span></span> | <span data-ttu-id="35b3f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="35b3f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35b3f-129">Header</span><span class="sxs-lookup"><span data-stu-id="35b3f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="35b3f-130"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="35b3f-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="35b3f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35b3f-131">Library</span></span><br/> | <dl> <span data-ttu-id="35b3f-132"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35b3f-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35b3f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35b3f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35b3f-134">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="35b3f-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="35b3f-135">**Iportablede vicevalues:: removeValue**</span><span class="sxs-lookup"><span data-stu-id="35b3f-135">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> <dt>

[<span data-ttu-id="35b3f-136">**Iportabledebug:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="35b3f-136">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




