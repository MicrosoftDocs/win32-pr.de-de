---
title: Wiedergabe. appendItem-Methode
description: Mit der appendItem-Methode wird am Ende der Wiedergabeliste ein Medien Element hinzugefügt.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- appendItem-Methode, Windows Media Player
- appendItem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, appendItem-Methode
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 828799d5b6e71e7ff0e7be4c1e55714f6343be51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358359"
---
# <a name="playlistappenditem-method"></a><span data-ttu-id="78d31-106">Wiedergabe. appendItem-Methode</span><span class="sxs-lookup"><span data-stu-id="78d31-106">Playlist.appendItem method</span></span>

<span data-ttu-id="78d31-107">Mit der **appendItem** -Methode wird am Ende der Wiedergabeliste ein Medien Element hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="78d31-107">The **appendItem** method adds a media item to the end of the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d31-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="78d31-108">Syntax</span></span>


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="78d31-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="78d31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d31-110">*Element* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78d31-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78d31-111">Das hinzu zufügende **Medien** Objekt.</span><span class="sxs-lookup"><span data-stu-id="78d31-111">**Media** object to be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d31-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78d31-112">Return value</span></span>

<span data-ttu-id="78d31-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78d31-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78d31-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78d31-114">Remarks</span></span>

<span data-ttu-id="78d31-115">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="78d31-115">To use this method, full access to the library is required.</span></span> <span data-ttu-id="78d31-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="78d31-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="78d31-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78d31-117">Examples</span></span>

<span data-ttu-id="78d31-118">Im folgenden JScript-Beispiel wird die *Wiedergabeliste* verwendet. **appendItem** , um der Wiedergabeliste mit dem Namen "threelist" das aktuelle Medien Element hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="78d31-118">The following JScript example uses *Playlist*.**appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="78d31-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="78d31-119">The **Player** object was created with ID="Player".</span></span>


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a><span data-ttu-id="78d31-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78d31-120">Requirements</span></span>



| <span data-ttu-id="78d31-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78d31-121">Requirement</span></span> | <span data-ttu-id="78d31-122">Wert</span><span class="sxs-lookup"><span data-stu-id="78d31-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="78d31-123">Version</span><span class="sxs-lookup"><span data-stu-id="78d31-123">Version</span></span><br/> | <span data-ttu-id="78d31-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="78d31-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="78d31-125">DLL</span><span class="sxs-lookup"><span data-stu-id="78d31-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="78d31-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78d31-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d31-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78d31-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d31-128">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="78d31-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="78d31-129">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="78d31-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="78d31-130">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="78d31-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





