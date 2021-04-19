---
title: Media. isread onlyitem-Methode
description: Die isread onlyitem-Methode gibt einen Wert zurück, der angibt, ob das angegebene Attribut des Medien Elements bearbeitet werden kann.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- isread onlyitem-Methode, Windows Media Player
- isleseronlyitem-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, isumonlyitem-Methode
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363199"
---
# <a name="mediaisreadonlyitem-method"></a><span data-ttu-id="c7c45-106">Media. isread onlyitem-Methode</span><span class="sxs-lookup"><span data-stu-id="c7c45-106">Media.isReadOnlyItem method</span></span>

<span data-ttu-id="c7c45-107">Die **isread onlyitem** -Methode gibt einen Wert zurück, der angibt, ob das angegebene Attribut des Medien Elements bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7c45-107">The **isReadOnlyItem** method returns a value indicating whether the specified attribute of the media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c45-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c45-108">Syntax</span></span>


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="c7c45-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7c45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7c45-110">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7c45-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7c45-111">**Zeichenfolge** , die den Namen des zu testenden Attributs angibt.</span><span class="sxs-lookup"><span data-stu-id="c7c45-111">**String** indicating the name of the attribute to test.</span></span> <span data-ttu-id="c7c45-112">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="c7c45-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7c45-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7c45-113">Return value</span></span>

<span data-ttu-id="c7c45-114">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c7c45-114">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7c45-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7c45-115">Remarks</span></span>

<span data-ttu-id="c7c45-116">Wenn ein Attribut schreibgeschützt ist, kann es nicht mit der **setiteminfo** -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c7c45-116">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="c7c45-117">Beachten Sie, dass diese Methode möglicherweise unterschiedliche Werte für ein bestimmtes Attribut zurückgibt, wenn Sie mit verschiedenen Versionen von Windows Media Player verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7c45-117">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="c7c45-118">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c7c45-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="c7c45-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c7c45-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c7c45-120">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="c7c45-120">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="c7c45-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7c45-121">Examples</span></span>

<span data-ttu-id="c7c45-122">Im folgenden JScript-Beispiel werden *Medien* verwendet. " **isinfoonlyitem** ", um ein HTML-TEXTAREA-Element mit dem Namen "rwtext" mit Informationen zum aktuellen Medien Element auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="c7c45-122">The following JScript example uses *Media*.**isReadOnlyItem** to fill an HTML TEXTAREA element named rwText with information about the current media item.</span></span> <span data-ttu-id="c7c45-123">Der Code gibt jedes Attribut des aktuellen Medien Elements zusammen mit Text aus, der angibt, ob das Attribut schreibgeschützt ist oder Lese-/Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="c7c45-123">The code outputs each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="c7c45-124">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="c7c45-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="c7c45-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c7c45-125">Requirements</span></span>



| <span data-ttu-id="c7c45-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c7c45-126">Requirement</span></span> | <span data-ttu-id="c7c45-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c7c45-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c45-128">Version</span><span class="sxs-lookup"><span data-stu-id="c7c45-128">Version</span></span><br/> | <span data-ttu-id="c7c45-129">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c7c45-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c7c45-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c45-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="c7c45-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c45-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7c45-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7c45-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c45-133">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="c7c45-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="c7c45-134">**"Media. mentiteminfo"**</span><span class="sxs-lookup"><span data-stu-id="c7c45-134">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="c7c45-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="c7c45-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c7c45-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="c7c45-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





