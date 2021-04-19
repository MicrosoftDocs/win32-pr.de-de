---
title: Media. getItemInfoByType-Methode
description: Die getItemInfoByType-Methode ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362101"
---
# <a name="mediagetiteminfobytype-method"></a><span data-ttu-id="7d341-106">Media. getItemInfoByType-Methode</span><span class="sxs-lookup"><span data-stu-id="7d341-106">Media.getItemInfoByType method</span></span>

<span data-ttu-id="7d341-107">Die **getItemInfoByType** -Methode ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="7d341-107">The **getItemInfoByType** method retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d341-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d341-108">Syntax</span></span>


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a><span data-ttu-id="7d341-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d341-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d341-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d341-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d341-111">**Zeichenfolge** , die den Namen des Attributs enthält.</span><span class="sxs-lookup"><span data-stu-id="7d341-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="7d341-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="7d341-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d341-113">*Sprache* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d341-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d341-114">**Zeichenfolge** , die die Sprache darstellt.</span><span class="sxs-lookup"><span data-stu-id="7d341-114">**String** representing the language.</span></span> <span data-ttu-id="7d341-115">Wenn der Wert auf NULL oder "" (leere Zeichenfolge) festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d341-115">If the value is set to null or "" (empty string) the current locale string is used.</span></span> <span data-ttu-id="7d341-116">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="7d341-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="7d341-117">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d341-117">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d341-118">**Number** (**Long**), der den NULL basierten Index des Werts enthält, der aus dem Attribut abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d341-118">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d341-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d341-119">Return value</span></span>

<span data-ttu-id="7d341-120">Diese Methode gibt eine **Zahl**, ein **Zeichen** folgen Objekt, ein **MetadataPicture** -Objekt oder ein **MetadataText** -Objekt zurück, wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="7d341-120">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="7d341-121">Attribut</span><span class="sxs-lookup"><span data-stu-id="7d341-121">Attribute</span></span>                   | <span data-ttu-id="7d341-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7d341-122">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="7d341-123">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="7d341-123">**SyncState**</span></span>               | <span data-ttu-id="7d341-124">**Number** (**Ganzzahl ohne Vorzeichen long**)</span><span class="sxs-lookup"><span data-stu-id="7d341-124">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="7d341-125">**Synchronisierte WM/Liedtexte \_**</span><span class="sxs-lookup"><span data-stu-id="7d341-125">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="7d341-126">**MetadataText** -Objekt</span><span class="sxs-lookup"><span data-stu-id="7d341-126">**MetadataText** object</span></span>        |
| <span data-ttu-id="7d341-127">**WM/Bild**</span><span class="sxs-lookup"><span data-stu-id="7d341-127">**WM/Picture**</span></span>              | <span data-ttu-id="7d341-128">**MetadataPicture** -Objekt</span><span class="sxs-lookup"><span data-stu-id="7d341-128">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="7d341-129">**WM/userweburl**</span><span class="sxs-lookup"><span data-stu-id="7d341-129">**WM/UserWebURL**</span></span>           | <span data-ttu-id="7d341-130">**MetadataText** -Objekt</span><span class="sxs-lookup"><span data-stu-id="7d341-130">**MetadataText** object</span></span>        |
| <span data-ttu-id="7d341-131">Alle anderen Attribute</span><span class="sxs-lookup"><span data-stu-id="7d341-131">All other attributes</span></span>        | <span data-ttu-id="7d341-132">**String**</span><span class="sxs-lookup"><span data-stu-id="7d341-132">**String**</span></span>                     |



 

<span data-ttu-id="7d341-133">Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, gibt diese Methode die Zeichenfolge "true" oder "false" zurück.</span><span class="sxs-lookup"><span data-stu-id="7d341-133">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="7d341-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7d341-134">Remarks</span></span>

<span data-ttu-id="7d341-135">Diese Methode ruft die Metadaten für ein einzelnes digitales Medien Element oder ein Medien Element ab, das Teil einer Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="7d341-135">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="7d341-136">Diese Methode unterstützt Attribute mit mehreren Werten und Attributen mit komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="7d341-136">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="7d341-137">Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren Werten und Attributen mit komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="7d341-137">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="7d341-138">Die **AttributeCount** -Eigenschaft enthält die Anzahl von Attributnamen, die für ein bestimmtes **Medien** Objekt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7d341-138">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="7d341-139">Index Nummern können dann mit der **GetAttributeName** -Methode verwendet werden, um den Namen der einzelnen verfügbaren Attribute zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7d341-139">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="7d341-140">Einzelne Attributnamen können an den *Name* -Parameter von **getItemInfoByType** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d341-140">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="7d341-141">Die **getattributezähltbytype** -Methode gibt die Anzahl von Attributen zurück, die einem bestimmten Attributnamen für ein bestimmtes **Medien** Objekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7d341-141">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="7d341-142">Indexnummern können dann an den *Index* -Parameter von **getItemInfoByType** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7d341-142">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="7d341-143">Dies ist hilfreich, wenn ein digitales Medien Element z. b. unter mehreren Genres kategorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7d341-143">This is useful when a digital media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="7d341-144">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d341-144">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7d341-145">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7d341-145">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7d341-146">Diese Methode kann zu Fehlern führen.</span><span class="sxs-lookup"><span data-stu-id="7d341-146">This method can cause errors.</span></span> <span data-ttu-id="7d341-147">Wenn Sie diese Methode aufgerufen haben, sollten Sie Fehler Behandlungs Code einschließen.</span><span class="sxs-lookup"><span data-stu-id="7d341-147">You should include error-handling code when you call this method.</span></span> <span data-ttu-id="7d341-148">In JScript können Sie z. b. die Fehlerbehandlung mithilfe von **try... catch... Abschließend** Struktur.</span><span class="sxs-lookup"><span data-stu-id="7d341-148">For example, in JScript you can implement error handling by using the **try...catch...finally** structure.</span></span>

<span data-ttu-id="7d341-149">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d341-149">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d341-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d341-150">Requirements</span></span>



| <span data-ttu-id="7d341-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d341-151">Requirement</span></span> | <span data-ttu-id="7d341-152">Wert</span><span class="sxs-lookup"><span data-stu-id="7d341-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d341-153">Version</span><span class="sxs-lookup"><span data-stu-id="7d341-153">Version</span></span><br/> | <span data-ttu-id="7d341-154">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7d341-154">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="7d341-155">DLL</span><span class="sxs-lookup"><span data-stu-id="7d341-155">DLL</span></span><br/>     | <dl> <span data-ttu-id="7d341-156"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d341-156"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d341-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d341-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d341-158">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="7d341-158">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7d341-159">**Media. AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="7d341-159">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="7d341-160">**Media. getattributecountrytbytype**</span><span class="sxs-lookup"><span data-stu-id="7d341-160">**Media.getAttributeCountByType**</span></span>](media-getattributecountbytype.md)
</dt> <dt>

[<span data-ttu-id="7d341-161">**Media. GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="7d341-161">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="7d341-162">**Media. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="7d341-162">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="7d341-163">**"Media. mentiteminfo"**</span><span class="sxs-lookup"><span data-stu-id="7d341-163">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="7d341-164">**MetadataPicture-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7d341-164">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="7d341-165">**MetadataText-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7d341-165">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="7d341-166">**Lesen von Attributwerten**</span><span class="sxs-lookup"><span data-stu-id="7d341-166">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="7d341-167">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="7d341-167">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7d341-168">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="7d341-168">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





