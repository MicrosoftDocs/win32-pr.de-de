---
title: Mediacollection. getByName-Methode
description: Die getByName-Methode ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Namen ab.
ms.assetid: f9395a4f-06d6-438b-b7c5-7a063abdf59f
keywords:
- getByName-Methode, Windows-Media Player
- getByName-Methode, Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, getByName-Methode
topic_type:
- apiref
api_name:
- MediaCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a3fc6e34b508fa094f79d2fbbd1d44ab712789
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366032"
---
# <a name="mediacollectiongetbyname-method"></a><span data-ttu-id="4e99b-106">Mediacollection. getByName-Methode</span><span class="sxs-lookup"><span data-stu-id="4e99b-106">MediaCollection.getByName method</span></span>

<span data-ttu-id="4e99b-107">Die **getByName** -Methode ruft eine Wiedergabeliste der Medienelemente mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="4e99b-107">The **getByName** method retrieves a playlist of the media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e99b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e99b-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByName(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="4e99b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e99b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e99b-110">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e99b-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e99b-111">**Zeichenfolge** , die den Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="4e99b-111">**String** containing the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e99b-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e99b-112">Return value</span></span>

<span data-ttu-id="4e99b-113">Diese Methode gibt ein **Wiedergabe** Listen Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="4e99b-113">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e99b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e99b-114">Remarks</span></span>

<span data-ttu-id="4e99b-115">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4e99b-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="4e99b-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4e99b-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4e99b-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e99b-117">Examples</span></span>

<span data-ttu-id="4e99b-118">Im folgenden JScript-Beispiel wird *mediacollection* verwendet. **getByName** , um drei Elemente aus der Bibliothek abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e99b-118">The following JScript example uses *MediaCollection*.**getByName** to retrieve three items from the library.</span></span> <span data-ttu-id="4e99b-119">Jedes Element wird dann an die aktuelle Wiedergabeliste angehängt.</span><span class="sxs-lookup"><span data-stu-id="4e99b-119">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="4e99b-120">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e99b-120">The **Player** object was created with ID="Player".</span></span>


```JScript
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get a playlist object that contains an Internet URL.
var One = Player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");
 
// Get a playlist object that contains a file on a network server.
var Two = Player.mediaCollection.getByName("Jeanne");

// Get a playlist object that contains a file on a local drive.
var Three = Player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use Playlist.item with
// an index of zero to reference that item.
Player.currentPlaylist.appendItem(One.item(0));
Player.currentPlaylist.appendItem(Two.item(0));
Player.currentPlaylist.appendItem(Three.item(0));

```



## <a name="requirements"></a><span data-ttu-id="4e99b-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e99b-121">Requirements</span></span>



| <span data-ttu-id="4e99b-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e99b-122">Requirement</span></span> | <span data-ttu-id="4e99b-123">Wert</span><span class="sxs-lookup"><span data-stu-id="4e99b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e99b-124">Version</span><span class="sxs-lookup"><span data-stu-id="4e99b-124">Version</span></span><br/> | <span data-ttu-id="4e99b-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4e99b-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4e99b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4e99b-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="4e99b-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e99b-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e99b-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e99b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e99b-129">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4e99b-129">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="4e99b-130">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="4e99b-130">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="4e99b-131">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="4e99b-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="4e99b-132">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="4e99b-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





