---
description: Die CompareTo- \_ Methode des-Objekts von "errbemjebject" vergleicht zwei "errbemujebject"-Objekte Dieser Vergleich unterliegt bestimmten Einschränkungen basierend auf den Werten, die im IFlags-Parameter angegeben sind.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: SWbemObject.CompareTo_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755016"
---
# <a name="swbemobjectcompareto_-method"></a><span data-ttu-id="c8473-104">Errbemubject. CompareTo- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="c8473-104">SWbemObject.CompareTo\_ method</span></span>

<span data-ttu-id="c8473-105">Die **CompareTo \_** -Methode des-Objekts von " [**errbemjebject**](swbemobject.md) " vergleicht zwei " **errbemujebject** "-Objekte</span><span class="sxs-lookup"><span data-stu-id="c8473-105">The **CompareTo\_** method of the [**SWbemObject**](swbemobject.md) object compares two **SWbemObject** objects.</span></span> <span data-ttu-id="c8473-106">Dieser Vergleich unterliegt bestimmten Einschränkungen basierend auf den Werten, die im *IFlags* -Parameter angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c8473-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="c8473-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c8473-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8473-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8473-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c8473-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8473-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8473-110">*objwbemujekt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8473-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8473-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c8473-111">Required.</span></span> <span data-ttu-id="c8473-112">Bei diesem Parameter handelt es sich um ein Objekt vom Typ " [**Swap**](swbemobject.md) "</span><span class="sxs-lookup"><span data-stu-id="c8473-112">This parameter is an [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="c8473-113">Dies ist das Objekt, mit dem das erste Objekt verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="c8473-113">This is the object with which the first object is compared.</span></span> <span data-ttu-id="c8473-114">Das Objekt muss eine gültige Instanz von " **errbemubject** " sein.</span><span class="sxs-lookup"><span data-stu-id="c8473-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="c8473-115">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c8473-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8473-116">Gibt die Objekteigenschaften an, die beim Vergleich eines Objekts mit anderen Objekten zu beachten sind.</span><span class="sxs-lookup"><span data-stu-id="c8473-116">Specifies the object characteristics to consider when comparing an object with other objects.</span></span> <span data-ttu-id="c8473-117">Sie können mit **wbemcomparisonflagincludeall** alle Features (Standardeinstellung) oder eine beliebige Kombination der folgenden Werte in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="c8473-117">You can use **wbemComparisonFlagIncludeAll** to consider all features (this is the default), or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="c8473-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemcomparisonflagincluentall \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c8473-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c8473-119">Vergleicht alle Eigenschaften, Qualifizierer und Varianten.</span><span class="sxs-lookup"><span data-stu-id="c8473-119">Compares all properties, qualifiers, and flavors.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="c8473-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemcomparisonflagignoreobjectsource \* \* \* \* (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="c8473-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="c8473-121">Bewirkt, dass die Quelle der Objekte, nämlich der Server und der Namespace, von denen Sie stammen, im Vergleich zu anderen Objekten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c8473-121">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="c8473-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemcomparisonflagignorequalifizierer \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="c8473-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="c8473-123">Bewirkt, dass alle Qualifizierer (einschließlich **Key** und **Dynamic**) im Vergleich ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c8473-123">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="c8473-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemcomparisonflagignoredefaultvalues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="c8473-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="c8473-125">Bewirkt, dass Standardwerte von Eigenschaften ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c8473-125">Causes default values of properties to be ignored.</span></span> <span data-ttu-id="c8473-126">Dieses Flag ist nur beim Vergleich von Klassen sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="c8473-126">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="c8473-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemcomparisonflagignoreflavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="c8473-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="c8473-128">Bewirkt, dass qualifizierervarianten ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="c8473-128">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="c8473-129">Dieses Flag nimmt die Qualifiziererwerte in Betracht, ignoriert jedoch die Unterschiede bei der Konfiguration, wie z. b</span><span class="sxs-lookup"><span data-stu-id="c8473-129">This flag takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="c8473-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemcomparisonflagignorecase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="c8473-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="c8473-131">Vergleicht Zeichen folgen Werte ohne Berücksichtigung der Groß-und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="c8473-131">Compares string values in a case-insensitive manner.</span></span> <span data-ttu-id="c8473-132">Dies gilt sowohl für Zeichen folgen als auch für Qualifiziererwerte.</span><span class="sxs-lookup"><span data-stu-id="c8473-132">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="c8473-133">Unabhängig davon, ob dieses Flag angegeben ist, werden Eigenschaften- und Qualifizierernamen immer ohne Berücksichtigung von Groß- und Kleinschreibung verglichen.</span><span class="sxs-lookup"><span data-stu-id="c8473-133">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="c8473-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemcomparisonflagignoreclass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="c8473-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="c8473-135">Weist das System an, davon auszugehen, dass es sich bei den verglichenen Objekten um Instanzen derselben Klasse handelt.</span><span class="sxs-lookup"><span data-stu-id="c8473-135">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="c8473-136">Folglich vergleicht dieses Flag nur instanzbezogene Informationen.</span><span class="sxs-lookup"><span data-stu-id="c8473-136">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="c8473-137">Mithilfe dieses Flags können Sie die Leistung optimieren.</span><span class="sxs-lookup"><span data-stu-id="c8473-137">Use this flag to optimize performance.</span></span> <span data-ttu-id="c8473-138">Wenn die Objekte nicht zu derselben Klasse gehören, sind die Ergebnisse undefiniert.</span><span class="sxs-lookup"><span data-stu-id="c8473-138">If the objects are not of the same class, the results are undefined.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8473-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8473-139">Return value</span></span>

<span data-ttu-id="c8473-140">Diese Methode gibt den booleschen Wert **true** zurück, wenn die Objekte mit identisch sind.</span><span class="sxs-lookup"><span data-stu-id="c8473-140">This method returns the Boolean value of **TRUE** if the objects match.</span></span> <span data-ttu-id="c8473-141">Gibt **false** zurück, wenn die Objekte nicht stimmen.</span><span class="sxs-lookup"><span data-stu-id="c8473-141">It returns **FALSE** if the objects do not match.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8473-142">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="c8473-142">Error codes</span></span>

<span data-ttu-id="c8473-143">Nach dem Abschluss der **CompareTo \_** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="c8473-143">After the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c8473-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c8473-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c8473-145">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c8473-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c8473-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c8473-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c8473-147">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c8473-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c8473-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c8473-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c8473-149">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c8473-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8473-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8473-150">Requirements</span></span>



| <span data-ttu-id="c8473-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8473-151">Requirement</span></span> | <span data-ttu-id="c8473-152">Wert</span><span class="sxs-lookup"><span data-stu-id="c8473-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8473-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c8473-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c8473-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8473-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8473-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c8473-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c8473-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8473-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8473-157">Header</span><span class="sxs-lookup"><span data-stu-id="c8473-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8473-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8473-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8473-159">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c8473-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8473-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c8473-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c8473-161">DLL</span><span class="sxs-lookup"><span data-stu-id="c8473-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8473-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8473-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c8473-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="c8473-163">CLSID</span></span><br/>                    | <span data-ttu-id="c8473-164">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="c8473-164">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c8473-165">IID</span><span class="sxs-lookup"><span data-stu-id="c8473-165">IID</span></span><br/>                      | <span data-ttu-id="c8473-166">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="c8473-166">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c8473-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8473-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8473-168">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="c8473-168">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




