---
description: Die Add-Methode des-Objekts von "Swap. Set" fügt der Auflistung von "taubemqualifierset" ein "taubemqualifier"-Objekt hinzu. Wenn ein Qualifizierer mit dem gleichen Namen bereits in der Auflistung vorhanden ist, wird er ersetzt.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Taubemqualifierset. Add-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349199"
---
# <a name="swbemqualifiersetadd-method"></a><span data-ttu-id="3a096-104">Taubemqualifierset. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="3a096-104">SWbemQualifierSet.Add method</span></span>

<span data-ttu-id="3a096-105">Die **Add** -Methode des-Objekts von " [**Swap. set**](swbemqualifierset.md) " fügt der Auflistung von "taubemqualifierset" ein "  [**taubemqualifier**](swbemqualifier.md) "-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="3a096-105">The **Add** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span> <span data-ttu-id="3a096-106">Wenn ein Qualifizierer mit dem gleichen Namen bereits in der Auflistung vorhanden ist, wird er ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3a096-106">If a qualifier with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="3a096-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3a096-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a096-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a096-108">Syntax</span></span>


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3a096-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a096-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a096-110">" *Name* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="3a096-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a096-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a096-111">Required.</span></span> <span data-ttu-id="3a096-112">Der Name des neuen Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="3a096-112">Name of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-113">*varval* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a096-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a096-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3a096-114">Required.</span></span> <span data-ttu-id="3a096-115">Der Variant-Wert des neuen Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="3a096-115">Variant value of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-116">*bpropagatestosubclasses* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3a096-116">*bPropagatesToSubclasses* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a096-117">Boolescher Wert, der angibt, ob dieser neue Qualifizierer an Unterklassen weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a096-117">Boolean value that indicates if this new qualifier is propagated to subclasses.</span></span> <span data-ttu-id="3a096-118">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="3a096-118">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-119">*bpropagatestoinstance* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3a096-119">*bPropagatesToInstances* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a096-120">Boolescher Wert, der angibt, ob dieser neue Qualifizierer an-Instanzen weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a096-120">Boolean value that indicates if this new qualifier is propagated to instances.</span></span> <span data-ttu-id="3a096-121">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="3a096-121">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-122">*boverridable* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3a096-122">*bOverridable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a096-123">Boolescher Wert, der angibt, ob dieser Qualifizierer bei der Weitergabe überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a096-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span> <span data-ttu-id="3a096-124">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="3a096-124">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-125">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="3a096-125">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3a096-126">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="3a096-126">Reserved.</span></span> <span data-ttu-id="3a096-127">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3a096-127">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a096-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a096-128">Return value</span></span>

<span data-ttu-id="3a096-129">Bei erfolgreicher Ausführung gibt diese [**Methode ein-**](swbemqualifier.md) Objekt zurück, das den neuen Qualifizierer darstellt.</span><span class="sxs-lookup"><span data-stu-id="3a096-129">If successful, this method returns an [**SWbemQualifier**](swbemqualifier.md) object that represents the new qualifier.</span></span> <span data-ttu-id="3a096-130">Andernfalls wird ein **null** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3a096-130">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a096-131">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="3a096-131">Error codes</span></span>

<span data-ttu-id="3a096-132">Nach Abschluss der **Add** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="3a096-132">After completion of the **Add** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="3a096-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="3a096-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="3a096-134">Der *IFlags* -Parameter war ungültig.</span><span class="sxs-lookup"><span data-stu-id="3a096-134">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-135">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="3a096-135">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="3a096-136">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3a096-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-137">**wbemErrCannotBeKey** -2147749919 (0x8004101f)</span><span class="sxs-lookup"><span data-stu-id="3a096-137">**wbemErrCannotBeKey** - 2147749919 (0x8004101F)</span></span>
</dt> <dd>

<span data-ttu-id="3a096-138">Es wurde ein unzulässiger Versuch unternommen, einen **Schlüssel** Qualifizierer für eine Eigenschaft anzugeben, die kein Schlüssel sein kann.</span><span class="sxs-lookup"><span data-stu-id="3a096-138">There was an illegal attempt to specify a **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="3a096-139">Die Schlüssel sind in der Klassendefinition für ein Objekt angegeben und können nicht für jede Instanz einzeln geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3a096-139">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-140">**wbemErrInvalidQualifierType** -2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="3a096-140">**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)</span></span>
</dt> <dd>

<span data-ttu-id="3a096-141">Der *varval* -Parameter ist kein gültiger qualifizierungstyp.</span><span class="sxs-lookup"><span data-stu-id="3a096-141">The *varVal* parameter is not of a legal qualifier type.</span></span>

</dd> <dt>

<span data-ttu-id="3a096-142">**wbemErrOverrideNotAllowed** -2147749914 (0x8004101a)</span><span class="sxs-lookup"><span data-stu-id="3a096-142">**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)</span></span>
</dt> <dd>

<span data-ttu-id="3a096-143">Es ist nicht möglich, den Vorgang " **taubemqualifierset. Add** " für diesen Qualifizierer auszuführen, da das besitzende Objekt keine über schreibungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="3a096-143">It is not possible to perform the **SWbemQualifierSet.Add** operation on this qualifier because the owning object does not permit overrides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a096-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a096-144">Requirements</span></span>



| <span data-ttu-id="3a096-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a096-145">Requirement</span></span> | <span data-ttu-id="3a096-146">Wert</span><span class="sxs-lookup"><span data-stu-id="3a096-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a096-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a096-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3a096-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a096-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a096-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a096-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3a096-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a096-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a096-151">Header</span><span class="sxs-lookup"><span data-stu-id="3a096-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a096-152"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a096-152"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a096-153">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3a096-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a096-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3a096-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3a096-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3a096-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a096-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a096-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3a096-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="3a096-157">CLSID</span></span><br/>                    | <span data-ttu-id="3a096-158">CLSID- \_ Swap-Gruppe</span><span class="sxs-lookup"><span data-stu-id="3a096-158">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="3a096-159">IID</span><span class="sxs-lookup"><span data-stu-id="3a096-159">IID</span></span><br/>                      | <span data-ttu-id="3a096-160">IID \_ iswbemqualifierset</span><span class="sxs-lookup"><span data-stu-id="3a096-160">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="3a096-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a096-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a096-162">**Swap-qualifierset**</span><span class="sxs-lookup"><span data-stu-id="3a096-162">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="3a096-163">**Swap-qualifierset. Remove**</span><span class="sxs-lookup"><span data-stu-id="3a096-163">**SWbemQualifierSet.Remove**</span></span>](swbemqualifierset-remove.md)
</dt> </dl>

 

 




