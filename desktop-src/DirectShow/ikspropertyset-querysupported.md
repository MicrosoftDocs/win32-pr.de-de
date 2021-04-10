---
description: Die querysupported-Methode bestimmt, ob ein Objekt einen angegebenen Eigenschaften Satz unterstützt.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Ikspropertyset:: querysupported-Methode (". h")'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213903"
---
# <a name="ikspropertysetquerysupported-method"></a><span data-ttu-id="c4316-103">Ikspropertyset:: querysupported-Methode</span><span class="sxs-lookup"><span data-stu-id="c4316-103">IKsPropertySet::QuerySupported method</span></span>

<span data-ttu-id="c4316-104">Die- `QuerySupported` Methode bestimmt, ob ein Objekt einen angegebenen Eigenschaften Satz unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4316-104">The `QuerySupported` method determines whether an object supports a specified property set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4316-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4316-105">Syntax</span></span>


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a><span data-ttu-id="c4316-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4316-107">*guidpropset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4316-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4316-108">Eigenschaften Satz-GUID.</span><span class="sxs-lookup"><span data-stu-id="c4316-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="c4316-109">*dwpropid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4316-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4316-110">Der Bezeichner der Eigenschaft innerhalb des Eigenschaften Satzes.</span><span class="sxs-lookup"><span data-stu-id="c4316-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="c4316-111">*ptypesupport* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4316-111">*pTypeSupport* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4316-112">Ein Zeiger auf einen Wert, in dem Flags gespeichert werden, die die vom Treiber bereitgestellte Unterstützung angeben.</span><span class="sxs-lookup"><span data-stu-id="c4316-112">Pointer to a value in which to store flags indicating the support provided by the driver.</span></span> <span data-ttu-id="c4316-113">Folgende Flags werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c4316-113">Supported flags include the following.</span></span>



| <span data-ttu-id="c4316-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c4316-114">Value</span></span>                    | <span data-ttu-id="c4316-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4316-115">Description</span></span>                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4316-116">ksproperty- \_ Unterstützung abrufen \_</span><span class="sxs-lookup"><span data-stu-id="c4316-116">KSPROPERTY\_SUPPORT\_GET</span></span> | <span data-ttu-id="c4316-117">Sie können die-Eigenschaft abrufen, indem Sie die " [**ikspropertyset:: Get**](ikspropertyset-get.md) "-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c4316-117">You can retrieve the property by calling the [**IKsPropertySet::Get**](ikspropertyset-get.md) method.</span></span> |
| <span data-ttu-id="c4316-118">ksproperty- \_ Unterstützungs \_ Satz</span><span class="sxs-lookup"><span data-stu-id="c4316-118">KSPROPERTY\_SUPPORT\_SET</span></span> | <span data-ttu-id="c4316-119">Sie können die Eigenschaft ändern, indem Sie " [**ikspropertyset:: Set**](ikspropertyset-set.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c4316-119">You can change the property by calling [**IKsPropertySet::Set**](ikspropertyset-set.md).</span></span>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4316-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4316-120">Return value</span></span>

<span data-ttu-id="c4316-121">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c4316-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c4316-122">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="c4316-122">Possible values include the following.</span></span>



| <span data-ttu-id="c4316-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c4316-123">Return code</span></span>                                                                                              | <span data-ttu-id="c4316-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4316-124">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4316-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4316-125"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="c4316-126">Die angegebene Kombination aus Eigenschaften Satz und Eigenschaften-ID wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4316-126">The specified property set and property ID combination is supported.</span></span><br/> |
| <dl> <span data-ttu-id="c4316-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="c4316-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                | <span data-ttu-id="c4316-128">Der Eigenschaften Satz wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4316-128">Property set is not supported.</span></span><br/>                                       |
| <dl> <span data-ttu-id="c4316-129"><dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="c4316-129"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="c4316-130">Die eigen schafts-ID wird für den angegebenen Eigenschaften Satz nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4316-130">Property ID is not supported for the specified property set.</span></span><br/>         |
| <dl> <span data-ttu-id="c4316-131"><dt>**E- \_ Prop- \_ Satz \_ nicht unterstützt**</dt></span><span class="sxs-lookup"><span data-stu-id="c4316-131"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="c4316-132">Der Eigenschaften Satz wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c4316-132">Property set is not supported.</span></span><br/>                                       |



 

## <a name="remarks"></a><span data-ttu-id="c4316-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4316-133">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c4316-134">Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c4316-134">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="c4316-135">Die beiden Schnittstellen sind nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c4316-135">The two interfaces are not compatible.</span></span> <span data-ttu-id="c4316-136">Die im DirectShow-DDK dokumentierte " **ikscontrol** "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.</span><span class="sxs-lookup"><span data-stu-id="c4316-136">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="c4316-137">Sie müssen "KS. h" vor "ksproxy. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="c4316-137">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4316-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4316-138">Requirements</span></span>



| <span data-ttu-id="c4316-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4316-139">Requirement</span></span> | <span data-ttu-id="c4316-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c4316-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4316-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4316-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c4316-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4316-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                       |
| <span data-ttu-id="c4316-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4316-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c4316-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4316-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="c4316-145">Header</span><span class="sxs-lookup"><span data-stu-id="c4316-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4316-146"><dt>. H. </dt> <dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4316-146"><dt>Ks.h; </dt> <dt>Ksproxy.h</dt></span></span> </dl> |
| <span data-ttu-id="c4316-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4316-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4316-148"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c4316-148"><dt>Strmiids.lib</dt></span></span> </dl>                                                          |



## <a name="see-also"></a><span data-ttu-id="c4316-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4316-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4316-150">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="c4316-150">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="c4316-151">**"Ikspropertyset"-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c4316-151">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="c4316-152">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="c4316-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




