---
title: Mediacollection. IsDeleted-Methode
description: Die IsDeleted-Methode ruft einen Wert ab, der angibt, ob sich das angegebene Medien Element im Ordner "Gelöschte Elemente" befindet.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- IsDeleted-Methode (Windows Media Player)
- IsDeleted-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, IsDeleted-Methode
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352946"
---
# <a name="mediacollectionisdeleted-method"></a><span data-ttu-id="a4159-106">Mediacollection. IsDeleted-Methode</span><span class="sxs-lookup"><span data-stu-id="a4159-106">MediaCollection.isDeleted method</span></span>

<span data-ttu-id="a4159-107">Die **isDeleted** -Methode ruft einen Wert ab, der angibt, ob sich das angegebene Medien Element im Ordner "Gelöschte Elemente" befindet.</span><span class="sxs-lookup"><span data-stu-id="a4159-107">The **isDeleted** method retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4159-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4159-108">Syntax</span></span>


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="a4159-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4159-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4159-110">*Element* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4159-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4159-111">**Medien** Objekt, das möglicherweise gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a4159-111">**Media** object that might be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4159-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4159-112">Return value</span></span>

<span data-ttu-id="a4159-113">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a4159-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4159-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4159-114">Remarks</span></span>

<span data-ttu-id="a4159-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a4159-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a4159-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a4159-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a4159-117">**Windows Media Player 10 Mobile:** Diese Methode gibt immer **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="a4159-117">**Windows Media Player 10 Mobile:** This method always returns **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="a4159-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4159-118">Examples</span></span>

<span data-ttu-id="a4159-119">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **isDeleted** zum Testen, ob ein bestimmtes Medien Element, das in der Variablen mit dem Namen mediaobject gespeichert ist, im Ordner Gelöschte Elemente ist.</span><span class="sxs-lookup"><span data-stu-id="a4159-119">The following JScript example uses *MediaCollection*.**isDeleted** to test whether a particular media item, stored in the variable named mediaObject, is in the deleted items folder.</span></span> <span data-ttu-id="a4159-120">Wenn das Medien Element nicht bereits gelöscht wurde, wird es in den Ordner Gelöschte Elemente verschoben.</span><span class="sxs-lookup"><span data-stu-id="a4159-120">If the media item has not been deleted already, it is moved to the deleted items folder.</span></span> <span data-ttu-id="a4159-121">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4159-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="a4159-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4159-122">Requirements</span></span>



| <span data-ttu-id="a4159-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4159-123">Requirement</span></span> | <span data-ttu-id="a4159-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a4159-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4159-125">Version</span><span class="sxs-lookup"><span data-stu-id="a4159-125">Version</span></span><br/> | <span data-ttu-id="a4159-126">Windows Media Player Version 7,0, Windows Media Player Version 7,1 oder Windows Media Player für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4159-126">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="a4159-127">Diese Methode wird für Windows Media Player 9-Serie oder höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a4159-127">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="a4159-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a4159-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4159-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4159-129"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="a4159-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4159-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4159-131">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="a4159-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="a4159-132">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a4159-132">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a4159-133">**Mediacollection. SetDeleted**</span><span class="sxs-lookup"><span data-stu-id="a4159-133">**MediaCollection.setDeleted**</span></span>](mediacollection-setdeleted.md)
</dt> <dt>

[<span data-ttu-id="a4159-134">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="a4159-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a4159-135">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="a4159-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





