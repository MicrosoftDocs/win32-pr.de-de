---
description: Die CompareTo- \_ Methode des "errbemlasterror"-Objekts vergleicht zwei "errbeapbject"-Objekte. Dieser Vergleich unterliegt bestimmten Einschränkungen basierend auf den Werten, die im IFlags-Parameter angegeben sind.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: SWbemLastError.CompareTo_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347066"
---
# <a name="swbemlasterrorcompareto_-method"></a><span data-ttu-id="b821f-104">Methode ' Swap. CompareTo ' \_</span><span class="sxs-lookup"><span data-stu-id="b821f-104">SWbemLastError.CompareTo\_ method</span></span>

<span data-ttu-id="b821f-105">Die **CompareTo \_** -Methode des " [**errbemlasterror**](swbemlasterror.md) "-Objekts vergleicht zwei " [**errbeapbject**](swbemobject.md) "-Objekte.</span><span class="sxs-lookup"><span data-stu-id="b821f-105">The **CompareTo\_** method of the [**SWbemLastError**](swbemlasterror.md) object compares two [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="b821f-106">Dieser Vergleich unterliegt bestimmten Einschränkungen basierend auf den Werten, die im *IFlags* -Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="b821f-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="b821f-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b821f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b821f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b821f-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b821f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b821f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b821f-110">*objwbemujekt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b821f-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b821f-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b821f-111">Required.</span></span> <span data-ttu-id="b821f-112">Ein-Objekt der Klasse " [**Swap**](swbemobject.md) -Klasse".</span><span class="sxs-lookup"><span data-stu-id="b821f-112">An [**SWbemObject**](swbemobject.md) class object.</span></span> <span data-ttu-id="b821f-113">Dieser Parameter ist das Objekt, mit dem das erste Objekt verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="b821f-113">This parameter is the object with which the first object is compared.</span></span> <span data-ttu-id="b821f-114">Das Objekt muss eine gültige Instanz von " **errbemubject** " sein.</span><span class="sxs-lookup"><span data-stu-id="b821f-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="b821f-115">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b821f-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b821f-116">Eine ganze Zahl, die zusätzliche Flags für den Vorgang angibt.</span><span class="sxs-lookup"><span data-stu-id="b821f-116">An integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="b821f-117">Dieser Parameter gibt die Objekteigenschaften an, die bei der Objekt Vergleiche berücksichtigt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b821f-117">This parameter specifies the object characteristics to consider when object comparisons are made.</span></span> <span data-ttu-id="b821f-118">Mit **wbemcomparisonflagincludeall** können Sie alle Features (Standard) oder eine beliebige Kombination der folgenden Werte in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="b821f-118">You can use **wbemComparisonFlagIncludeAll** to consider all features (default) or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="b821f-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemcomparisonflagincluentall \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b821f-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b821f-120">Bewirkt, dass alle Eigenschaften, Qualifizierer und Variationen verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="b821f-120">Causes all properties, qualifiers, and flavors to be compared.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="b821f-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemcomparisonflagignorequalifizierer \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b821f-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b821f-122">Bewirkt, dass alle Qualifizierer (einschließlich **Key** und **Dynamic**) im Vergleich ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b821f-122">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="b821f-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemcomparisonflagignoreobjectsource \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="b821f-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="b821f-124">Bewirkt, dass die Quelle der Objekte, nämlich der Server und der Namespace, von denen Sie stammen, im Vergleich zu anderen Objekten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b821f-124">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="b821f-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemcomparisonflagignoredefaultvalues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="b821f-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="b821f-126">Bewirkt, dass die Standardwerte von Eigenschaften ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b821f-126">Causes the default values of properties to be ignored.</span></span> <span data-ttu-id="b821f-127">Dieses Flag ist nur beim Vergleich von Klassen sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="b821f-127">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="b821f-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemcomparisonflagignoreclass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="b821f-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="b821f-129">Weist das System an, davon auszugehen, dass es sich bei den verglichenen Objekten um Instanzen derselben Klasse handelt.</span><span class="sxs-lookup"><span data-stu-id="b821f-129">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="b821f-130">Folglich vergleicht dieses Flag nur instanzbezogene Informationen.</span><span class="sxs-lookup"><span data-stu-id="b821f-130">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="b821f-131">Mithilfe dieses Flags können Sie die Leistung optimieren.</span><span class="sxs-lookup"><span data-stu-id="b821f-131">Use this flag to optimize performance.</span></span> <span data-ttu-id="b821f-132">Wenn die Objekte nicht zu derselben Klasse gehören, sind die Ergebnisse undefiniert.</span><span class="sxs-lookup"><span data-stu-id="b821f-132">If the objects are not of the same class, the results are undefined.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="b821f-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemcomparisonflagignorecase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="b821f-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="b821f-134">Bewirkt, dass Zeichen folgen Werte ohne Beachtung der Groß-/Kleinschreibung verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="b821f-134">Causes string values to be compared in a case-insensitive manner.</span></span> <span data-ttu-id="b821f-135">Dies gilt sowohl für Zeichen folgen als auch für Qualifiziererwerte.</span><span class="sxs-lookup"><span data-stu-id="b821f-135">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="b821f-136">Unabhängig davon, ob dieses Flag angegeben ist, werden Eigenschaften- und Qualifizierernamen immer ohne Berücksichtigung von Groß- und Kleinschreibung verglichen.</span><span class="sxs-lookup"><span data-stu-id="b821f-136">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="b821f-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemcomparisonflagignoreflavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="b821f-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="b821f-138">Bewirkt, dass qualifizierervarianten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b821f-138">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="b821f-139">Dieses Flag berücksichtigt Qualifiziererwerte, ignoriert jedoch Unterschiede bei den verschiedenen Typen, z. B. Weitergaberegeln und Einschränkungen beim Überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b821f-139">This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b821f-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b821f-140">Return value</span></span>

<span data-ttu-id="b821f-141">Die **CompareTo \_** -Methode gibt den booleschen Wert **true** zurück, wenn die Objekte entsprechen; andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b821f-141">The **CompareTo\_** method returns the Boolean value **TRUE** if the objects match; otherwise, it returns **FALSE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b821f-142">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b821f-142">Error codes</span></span>

<span data-ttu-id="b821f-143">Nach dem Abschluss der **CompareTo \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="b821f-143">Upon the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b821f-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b821f-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b821f-145">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b821f-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b821f-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b821f-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b821f-147">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b821f-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b821f-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b821f-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b821f-149">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="b821f-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b821f-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b821f-150">Requirements</span></span>



| <span data-ttu-id="b821f-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b821f-151">Requirement</span></span> | <span data-ttu-id="b821f-152">Wert</span><span class="sxs-lookup"><span data-stu-id="b821f-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b821f-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b821f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="b821f-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b821f-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b821f-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b821f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="b821f-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b821f-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b821f-157">Header</span><span class="sxs-lookup"><span data-stu-id="b821f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="b821f-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b821f-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b821f-159">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b821f-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="b821f-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b821f-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b821f-161">DLL</span><span class="sxs-lookup"><span data-stu-id="b821f-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b821f-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b821f-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b821f-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="b821f-163">CLSID</span></span><br/>                    | <span data-ttu-id="b821f-164">CLSID- \_ Austausch Fehler</span><span class="sxs-lookup"><span data-stu-id="b821f-164">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="b821f-165">IID</span><span class="sxs-lookup"><span data-stu-id="b821f-165">IID</span></span><br/>                      | <span data-ttu-id="b821f-166">IID \_ iswbemlasterror</span><span class="sxs-lookup"><span data-stu-id="b821f-166">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="b821f-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b821f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b821f-168">**Austausch Fehler**</span><span class="sxs-lookup"><span data-stu-id="b821f-168">**SWbemLastError**</span></span>](swbemlasterror.md)
</dt> <dt>

[<span data-ttu-id="b821f-169">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="b821f-169">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




