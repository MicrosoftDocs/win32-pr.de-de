---
title: Mediacollection. Add-Methode
description: Die Add-Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu. | Mediacollection. Add-Methode
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Hinzufügen von Methoden Fenster Media Player
- Add-Methode Windows Media Player, mediacollection-Klasse
- Mediacollection-Klasse, Windows Media Player, Methode hinzufügen
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361364"
---
# <a name="mediacollectionadd-method"></a><span data-ttu-id="44084-107">Mediacollection. Add-Methode</span><span class="sxs-lookup"><span data-stu-id="44084-107">MediaCollection.add method</span></span>

<span data-ttu-id="44084-108">Die **Add** -Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="44084-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="44084-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="44084-109">Syntax</span></span>


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a><span data-ttu-id="44084-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="44084-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44084-111">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44084-111">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44084-112">**Zeichenfolge** , die den Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="44084-112">**String** containing the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44084-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44084-113">Return value</span></span>

<span data-ttu-id="44084-114">Diese Methode gibt ein **Medien** Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="44084-114">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44084-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44084-115">Remarks</span></span>

<span data-ttu-id="44084-116">Diese Methode lädt ein vorhandenes Medien Element oder eine vorhandene Wiedergabeliste in die Bibliothek, wenn ein Pfad zu einer Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="44084-116">This method loads an existing media item or playlist into the library, given a path to a file.</span></span> <span data-ttu-id="44084-117">Diese Methode verschiebt oder ändert die Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="44084-117">This method does not move or change the file.</span></span> <span data-ttu-id="44084-118">Bei dieser Methode tritt ein Fehler auf, wenn ein ungültiger lokaler Pfad vorliegt, aber digitale Mediendateien nicht auf Gültigkeit überprüft werden, bevor Sie der Bibliothek hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="44084-118">This method fails if given an invalid local path, but digital media files are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="44084-119">Diese Methode akzeptiert sowohl statische als auch automatische Wiedergabelisten Dateien.</span><span class="sxs-lookup"><span data-stu-id="44084-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="44084-120">Die *playlistcollection*. die **importwiedergabe** -Methode kann auch verwendet werden, um der Bibliothek eine statische Wiedergabeliste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="44084-120">The *PlaylistCollection*.**importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="44084-121">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="44084-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="44084-122">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="44084-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="44084-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44084-123">Examples</span></span>

<span data-ttu-id="44084-124">Im folgenden Microsoft JScript-Beispiel werden der Windows Media Player-Mediensammlung drei Medienobjekte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="44084-124">The following Microsoft JScript example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="44084-125">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="44084-125">The **Player** object was created with ID="Player".</span></span>


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a><span data-ttu-id="44084-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44084-126">Requirements</span></span>



| <span data-ttu-id="44084-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44084-127">Requirement</span></span> | <span data-ttu-id="44084-128">Wert</span><span class="sxs-lookup"><span data-stu-id="44084-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44084-129">Version</span><span class="sxs-lookup"><span data-stu-id="44084-129">Version</span></span><br/> | <span data-ttu-id="44084-130">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="44084-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="44084-131">DLL</span><span class="sxs-lookup"><span data-stu-id="44084-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="44084-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44084-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44084-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44084-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44084-134">**Verwalten von Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="44084-134">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="44084-135">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="44084-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="44084-136">**Mediacollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="44084-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="44084-137">**Mediacollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="44084-137">**MediaCollection.remove**</span></span>](mediacollection-remove.md)
</dt> <dt>

[<span data-ttu-id="44084-138">**Playlistcollection. importwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="44084-138">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="44084-139">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="44084-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="44084-140">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="44084-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





