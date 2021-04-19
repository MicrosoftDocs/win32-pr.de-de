---
title: StringCollection. getItemInfoByType-Methode
description: Die getItemInfoByType-Methode ruft den Wert ab, der dem angegebenen StringCollection-Index, dem angegebenen Namen, der angegebenen Sprache und dem angegebenen Attribut Index entspricht.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- getItemInfoByType-Methode, Windows Media Player
- getItemInfoByType-Methode, Windows Media Player, StringCollection-Klasse
- StringCollection-Klasse, Windows Media Player, getItemInfoByType-Methode
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366955"
---
# <a name="stringcollectiongetiteminfobytype-method"></a><span data-ttu-id="aa6ba-106">StringCollection. getItemInfoByType-Methode</span><span class="sxs-lookup"><span data-stu-id="aa6ba-106">StringCollection.getItemInfoByType method</span></span>

<span data-ttu-id="aa6ba-107">Die **getItemInfoByType** -Methode ruft den Wert ab, der dem angegebenen **StringCollection** -Index, dem angegebenen Namen, der angegebenen Sprache und dem angegebenen Attribut Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-107">The **getItemInfoByType** method retrieves the value corresponding to the specified **StringCollection** index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa6ba-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa6ba-108">Syntax</span></span>


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a><span data-ttu-id="aa6ba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa6ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa6ba-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa6ba-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6ba-111">**Number** (**Long**) gibt den NULL basierten Index des **StringCollection** -Elements an, aus dem das Attribut bezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="aa6ba-112">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa6ba-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6ba-113">**Zeichenfolge** , die den Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-113">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="aa6ba-114">*Sprache* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa6ba-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6ba-115">**Zeichenfolge** , die die Sprache enthält.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-115">**String** containing the language.</span></span> <span data-ttu-id="aa6ba-116">Wenn der Wert auf NULL oder eine leere Zeichenfolge ("") festgelegt ist, wird die aktuelle Gebiets Schema Zeichenfolge verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-116">If the value is set to null or the empty string ("") the current locale string is used.</span></span> <span data-ttu-id="aa6ba-117">Andernfalls muss der Wert eine gültige RFC 1766-sprach Zeichenfolge sein, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="aa6ba-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="aa6ba-118">*attributeIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aa6ba-118">*attributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa6ba-119">**Number** (**Long**), der den NULL basierten Index des Werts enthält, der aus dem Attribut abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-119">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa6ba-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa6ba-120">Return value</span></span>

<span data-ttu-id="aa6ba-121">Diese Methode gibt eine **Zahl**, ein **Zeichen** folgen Objekt, ein **MetadataPicture** -Objekt oder ein **MetadataText** -Objekt zurück, wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-121">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="aa6ba-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="aa6ba-122">Attribute</span></span>                   | <span data-ttu-id="aa6ba-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa6ba-123">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="aa6ba-124">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-124">**SyncState**</span></span>               | <span data-ttu-id="aa6ba-125">**Number** (**Ganzzahl ohne Vorzeichen long**)</span><span class="sxs-lookup"><span data-stu-id="aa6ba-125">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="aa6ba-126">**Synchronisierte WM/Liedtexte \_**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-126">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="aa6ba-127">**MetadataText** -Objekt</span><span class="sxs-lookup"><span data-stu-id="aa6ba-127">**MetadataText** object</span></span>        |
| <span data-ttu-id="aa6ba-128">**WM/Bild**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-128">**WM/Picture**</span></span>              | <span data-ttu-id="aa6ba-129">**MetadataPicture** -Objekt</span><span class="sxs-lookup"><span data-stu-id="aa6ba-129">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="aa6ba-130">**WM/userweburl**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-130">**WM/UserWebURL**</span></span>           | <span data-ttu-id="aa6ba-131">**MetadataText** -Objekt</span><span class="sxs-lookup"><span data-stu-id="aa6ba-131">**MetadataText** object</span></span>        |
| <span data-ttu-id="aa6ba-132">Alle anderen Attribute</span><span class="sxs-lookup"><span data-stu-id="aa6ba-132">All other attributes</span></span>        | <span data-ttu-id="aa6ba-133">String</span><span class="sxs-lookup"><span data-stu-id="aa6ba-133">String</span></span>                         |



 

<span data-ttu-id="aa6ba-134">Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, gibt diese Methode die Zeichenfolge "true" oder "false" zurück.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-134">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="aa6ba-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa6ba-135">Remarks</span></span>

<span data-ttu-id="aa6ba-136">Diese Methode unterstützt Attribute mit mehreren Werten und Attribute mit komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-136">This method supports attributes with multiple values, and attributes with complex values.</span></span> <span data-ttu-id="aa6ba-137">Die **getiteminfo** -Methode unterstützt keine Attribute mit mehreren oder komplexen Werten.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-137">The **getItemInfo** method does not support attributes with multiple or complex values.</span></span>

<span data-ttu-id="aa6ba-138">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-138">To use this method, read access to the library is required.</span></span> <span data-ttu-id="aa6ba-139">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="aa6ba-139">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa6ba-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa6ba-140">Requirements</span></span>



| <span data-ttu-id="aa6ba-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa6ba-141">Requirement</span></span> | <span data-ttu-id="aa6ba-142">Wert</span><span class="sxs-lookup"><span data-stu-id="aa6ba-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa6ba-143">Version</span><span class="sxs-lookup"><span data-stu-id="aa6ba-143">Version</span></span><br/> | <span data-ttu-id="aa6ba-144">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="aa6ba-144">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="aa6ba-145">DLL</span><span class="sxs-lookup"><span data-stu-id="aa6ba-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa6ba-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa6ba-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa6ba-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa6ba-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa6ba-148">**MetadataPicture-Objekt**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-148">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="aa6ba-149">**MetadataText-Objekt**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-149">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="aa6ba-150">**StringCollection. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-150">**StringCollection.getItemInfo**</span></span>](stringcollection-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="aa6ba-151">**StringCollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="aa6ba-151">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





