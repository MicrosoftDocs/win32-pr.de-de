---
title: Mediacollection. Remove-Methode
description: Die Remove-Methode entfernt ein Element aus der Medien Auflistung.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- Methode "Windows Media Player entfernen"
- Remove-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, Methode entfernen
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360397"
---
# <a name="mediacollectionremove-method"></a><span data-ttu-id="53e37-106">Mediacollection. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="53e37-106">MediaCollection.remove method</span></span>

<span data-ttu-id="53e37-107">Die **Remove** -Methode entfernt ein Element aus der Medien Auflistung.</span><span class="sxs-lookup"><span data-stu-id="53e37-107">The **remove** method removes an item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="53e37-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="53e37-108">Syntax</span></span>


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a><span data-ttu-id="53e37-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="53e37-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53e37-110">*Element* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53e37-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53e37-111">Das zu entfernende **Medien** Objekt.</span><span class="sxs-lookup"><span data-stu-id="53e37-111">**Media** object to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="53e37-112">*Löschen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53e37-112">*delete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53e37-113">**Boolescher** Wert, der angibt, ob das Element entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="53e37-113">**Boolean** indicating whether to remove the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53e37-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53e37-114">Return value</span></span>

<span data-ttu-id="53e37-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="53e37-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53e37-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53e37-116">Remarks</span></span>

<span data-ttu-id="53e37-117">Diese Methode löscht ein Element aus der Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="53e37-117">This method deletes an item from the library.</span></span> <span data-ttu-id="53e37-118">Mit dieser Methode werden keine Dateien auf dem Computer des Benutzers gelöscht.</span><span class="sxs-lookup"><span data-stu-id="53e37-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="53e37-119">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="53e37-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="53e37-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="53e37-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="53e37-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53e37-121">Examples</span></span>

<span data-ttu-id="53e37-122">Im folgenden JScript-Beispiel wird nach dem auffordern des Benutzers das erste Medien Element dauerhaft in der Mediensammlung mithilfe von *mediacollection* gelöscht. **Entfernen** Sie.</span><span class="sxs-lookup"><span data-stu-id="53e37-122">The following JScript example, after prompting the user, permanently deletes the first media item in the media collection by using *MediaCollection*.**remove**.</span></span> <span data-ttu-id="53e37-123">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="53e37-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a><span data-ttu-id="53e37-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53e37-124">Requirements</span></span>



| <span data-ttu-id="53e37-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53e37-125">Requirement</span></span> | <span data-ttu-id="53e37-126">Wert</span><span class="sxs-lookup"><span data-stu-id="53e37-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53e37-127">Version</span><span class="sxs-lookup"><span data-stu-id="53e37-127">Version</span></span><br/> | <span data-ttu-id="53e37-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="53e37-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="53e37-129">DLL</span><span class="sxs-lookup"><span data-stu-id="53e37-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="53e37-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53e37-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53e37-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53e37-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53e37-132">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="53e37-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="53e37-133">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="53e37-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="53e37-134">**Mediacollection. Add**</span><span class="sxs-lookup"><span data-stu-id="53e37-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="53e37-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="53e37-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="53e37-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="53e37-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





