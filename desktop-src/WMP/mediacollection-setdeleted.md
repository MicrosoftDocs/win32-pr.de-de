---
title: Mediacollection. SetDeleted-Methode
description: Die SetDeleted-Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente". | Mediacollection. SetDeleted-Methode
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- SetDeleted-Methoden Fenster Media Player
- SetDeleted-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, SetDeleted-Methode
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358360"
---
# <a name="mediacollectionsetdeleted-method"></a><span data-ttu-id="e2115-107">Mediacollection. SetDeleted-Methode</span><span class="sxs-lookup"><span data-stu-id="e2115-107">MediaCollection.setDeleted method</span></span>

<span data-ttu-id="e2115-108">Die **SetDeleted** -Methode verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".</span><span class="sxs-lookup"><span data-stu-id="e2115-108">The **setDeleted** method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2115-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2115-109">Syntax</span></span>


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a><span data-ttu-id="e2115-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2115-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2115-111">*Element* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2115-111">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2115-112">Das **Medien** Objekt, das verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e2115-112">**Media** object being moved.</span></span>

</dd> <dt>

<span data-ttu-id="e2115-113">*true* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2115-113">*true* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2115-114">Geben Sie diesen Wert immer an.</span><span class="sxs-lookup"><span data-stu-id="e2115-114">Always specify this value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2115-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2115-115">Return value</span></span>

<span data-ttu-id="e2115-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e2115-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2115-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2115-117">Remarks</span></span>

<span data-ttu-id="e2115-118">Mit dieser Methode werden Dateien nicht auf dem Computer des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="e2115-118">This method does not remove files from the user's computer.</span></span>

<span data-ttu-id="e2115-119">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2115-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="e2115-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e2115-120">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e2115-121">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2115-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="e2115-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2115-122">Examples</span></span>

<span data-ttu-id="e2115-123">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **SetDeleted** zum Verschieben eines bestimmten Medien Elements, das in der Variablen mit dem Namen "mediaobject" gespeichert ist, in den Ordner "Gelöschte Elemente".</span><span class="sxs-lookup"><span data-stu-id="e2115-123">The following JScript example uses *MediaCollection*.**setDeleted** to move a particular media item, stored in the variable named mediaObject, to the deleted items folder.</span></span> <span data-ttu-id="e2115-124">Die *mediacollection*. die **isDeleted** -Methode testet zunächst, ob das Element bereits gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="e2115-124">The *MediaCollection*.**isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="e2115-125">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e2115-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="e2115-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2115-126">Requirements</span></span>



| <span data-ttu-id="e2115-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2115-127">Requirement</span></span> | <span data-ttu-id="e2115-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e2115-128">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2115-129">Version</span><span class="sxs-lookup"><span data-stu-id="e2115-129">Version</span></span><br/> | <span data-ttu-id="e2115-130">Windows Media Player Version 7,0, Windows Media Player Version 7,1 oder Windows Media Player für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2115-130">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="e2115-131">Diese Methode wird für Windows Media Player 9-Serie oder höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2115-131">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="e2115-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e2115-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="e2115-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2115-133"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="e2115-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2115-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2115-135">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="e2115-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e2115-136">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="e2115-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="e2115-137">**Mediacollection. IsDeleted**</span><span class="sxs-lookup"><span data-stu-id="e2115-137">**MediaCollection.isDeleted**</span></span>](mediacollection-isdeleted.md)
</dt> <dt>

[<span data-ttu-id="e2115-138">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e2115-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e2115-139">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e2115-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





