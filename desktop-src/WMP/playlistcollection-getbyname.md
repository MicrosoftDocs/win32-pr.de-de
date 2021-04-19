---
title: Playlistcollection. getByName-Methode
description: Die getByName-Methode ruft ein playlistarray-Objekt ab, das Wiedergabelisten mit dem angegebenen Namen enthält (sofern vorhanden).
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- getByName-Methode, Windows-Media Player
- getByName-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, getByName-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366793"
---
# <a name="playlistcollectiongetbyname-method"></a><span data-ttu-id="9adee-106">Playlistcollection. getByName-Methode</span><span class="sxs-lookup"><span data-stu-id="9adee-106">PlaylistCollection.getByName method</span></span>

<span data-ttu-id="9adee-107">Die **getByName** -Methode ruft ein **playlistarray** -Objekt ab, das Wiedergabelisten mit dem angegebenen Namen enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="9adee-107">The **getByName** method retrieves a **PlaylistArray** object containing playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9adee-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9adee-108">Syntax</span></span>


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="9adee-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9adee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adee-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9adee-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adee-111">**Zeichenfolge** , die den Namen der abzurufenden Wiedergabelisten enthält.</span><span class="sxs-lookup"><span data-stu-id="9adee-111">**String** containing the name of the playlists to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adee-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9adee-112">Return value</span></span>

<span data-ttu-id="9adee-113">Diese Methode gibt ein **playlistarray** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9adee-113">This method returns a **PlaylistArray** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adee-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9adee-114">Remarks</span></span>

<span data-ttu-id="9adee-115">Verwenden Sie *playlistarray*. **Anzahl** , um zu bestimmen, ob eine Wiedergabeliste vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="9adee-115">Use *PlaylistArray*.**count** to determine whether a playlist exists.</span></span> <span data-ttu-id="9adee-116">Wenn **count** 0 (null) ist, ist keine Wiedergabeliste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9adee-116">If **count** is zero, a playlist does not exist.</span></span>

<span data-ttu-id="9adee-117">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9adee-117">To use this method, read access to the library is required.</span></span> <span data-ttu-id="9adee-118">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="9adee-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="9adee-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9adee-119">Examples</span></span>

<span data-ttu-id="9adee-120">Im folgenden JScript-Beispiel wird *playlistcollection* verwendet. **getByName** zum Überprüfen des **playlistcollection** -Objekts auf eine Wiedergabeliste mit dem Namen "threelist".</span><span class="sxs-lookup"><span data-stu-id="9adee-120">The following JScript example uses *playlistCollection*.**getByName** to check the **playlistCollection** object for a playlist named "ThreeList".</span></span> <span data-ttu-id="9adee-121">Wenn die Wiedergabeliste "threelist" vorhanden ist, legt **getByName** "threelist" als aktuelle Wiedergabeliste fest.</span><span class="sxs-lookup"><span data-stu-id="9adee-121">If the "Threelist" playlist exists, **getByName** sets "ThreeList" as the current playlist.</span></span> <span data-ttu-id="9adee-122">Das **Player** -Objekt wurde mit der ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="9adee-122">The **Player** object was created with the ID = "Player".</span></span>


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a><span data-ttu-id="9adee-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9adee-123">Requirements</span></span>



| <span data-ttu-id="9adee-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9adee-124">Requirement</span></span> | <span data-ttu-id="9adee-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9adee-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9adee-126">Version</span><span class="sxs-lookup"><span data-stu-id="9adee-126">Version</span></span><br/> | <span data-ttu-id="9adee-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9adee-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9adee-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9adee-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="9adee-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9adee-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9adee-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9adee-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9adee-131">**Playlistarray-Objekt**</span><span class="sxs-lookup"><span data-stu-id="9adee-131">**PlaylistArray Object**</span></span>](playlistarray-object.md)
</dt> <dt>

[<span data-ttu-id="9adee-132">**Playlistarray. Count**</span><span class="sxs-lookup"><span data-stu-id="9adee-132">**PlaylistArray.count**</span></span>](playlistarray-count.md)
</dt> <dt>

[<span data-ttu-id="9adee-133">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="9adee-133">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> <dt>

[<span data-ttu-id="9adee-134">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="9adee-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="9adee-135">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="9adee-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





