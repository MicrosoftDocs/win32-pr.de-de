---
description: Die Set-Methode legt eine Eigenschaft fest, die durch eine Eigenschaften Satz-GUID und eine Eigenschaften-ID identifiziert wird.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'Ikspropertyset:: Set-Methode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392605"
---
# <a name="ikspropertysetset-method"></a><span data-ttu-id="5e55c-103">Ikspropertyset:: Set-Methode</span><span class="sxs-lookup"><span data-stu-id="5e55c-103">IKsPropertySet::Set method</span></span>

<span data-ttu-id="5e55c-104">Die `Set` -Methode legt eine Eigenschaft fest, die durch eine Eigenschaften Satz-GUID und eine Eigenschaften-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5e55c-104">The `Set` method sets a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e55c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e55c-105">Syntax</span></span>


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a><span data-ttu-id="5e55c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e55c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e55c-107">*guidpropset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e55c-108">Eigenschaften Satz-GUID.</span><span class="sxs-lookup"><span data-stu-id="5e55c-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="5e55c-109">*dwpropid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e55c-110">Der Bezeichner der Eigenschaft innerhalb des Eigenschaften Satzes.</span><span class="sxs-lookup"><span data-stu-id="5e55c-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="5e55c-111">*pinstancedata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e55c-112">Zeiger auf einen Puffer, der Instanzdaten für die Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="5e55c-112">Pointer to a buffer that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="5e55c-113">*cbinstancedata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e55c-114">Größe des *pinstancedata* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5e55c-114">Size of the *pInstanceData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5e55c-115">*ppropdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-115">*pPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e55c-116">Zeiger auf einen Puffer, der den Wert der Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="5e55c-116">Pointer to a buffer that contains the value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="5e55c-117">*cbpropdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e55c-118">SISE des *ppropdata* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5e55c-118">Sise of the *pPropData* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e55c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e55c-119">Return value</span></span>

<span data-ttu-id="5e55c-120">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e55c-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5e55c-121">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="5e55c-121">Possible values include the following.</span></span>



| <span data-ttu-id="5e55c-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5e55c-122">Return code</span></span>                                                                                              | <span data-ttu-id="5e55c-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e55c-123">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e55c-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e55c-124"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="5e55c-125">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5e55c-125">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="5e55c-126"><dt>**E- \_ Prop- \_ Satz \_ nicht unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="5e55c-126"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="5e55c-127">Der Eigenschaften Satz wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e55c-127">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="5e55c-128"><dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="5e55c-128"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="5e55c-129">Die eigen schafts-ID wird für den angegebenen Eigenschaften Satz nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e55c-129">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e55c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e55c-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5e55c-131">Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5e55c-131">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="5e55c-132">Die beiden Schnittstellen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5e55c-132">The two interfaces are not compatible.</span></span> <span data-ttu-id="5e55c-133">Die im DirectShow-DDK dokumentierte " **ikscontrol** "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.</span><span class="sxs-lookup"><span data-stu-id="5e55c-133">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="5e55c-134">Sie müssen "KS. h" vor "ksproxy. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="5e55c-134">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e55c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e55c-135">Requirements</span></span>



| <span data-ttu-id="5e55c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e55c-136">Requirement</span></span> | <span data-ttu-id="5e55c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="5e55c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e55c-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e55c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5e55c-139">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5e55c-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e55c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5e55c-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e55c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5e55c-142">Header</span><span class="sxs-lookup"><span data-stu-id="5e55c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e55c-143"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e55c-143"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="5e55c-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e55c-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e55c-145"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="5e55c-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e55c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e55c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e55c-147">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="5e55c-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="5e55c-148">**"Ikspropertyset"-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5e55c-148">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="5e55c-149">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="5e55c-149">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




