---
title: Iwmpplaylistcollection importwiedergabe-Methode
description: Die importwiedergabe-Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu. | Iwmpplaylistcollection importwiedergabe-Methode
ms.assetid: 7a64e618-920d-419d-8769-612ab5dff49b
keywords:
- importwiedergabe-Methode, Windows-Media Player
- importwiedergabe-Methode, Windows Media Player, iwmpplaylistcollection-Schnittstelle
- Iwmpplaylistcollection-Schnittstelle Windows Media Player, importwiedergabe Methode
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.importPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ca727155d6ae859123d427812d93ebaa0b05c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350779"
---
# <a name="iwmpplaylistcollectionimportplaylist-method"></a><span data-ttu-id="c8888-107">Iwmpplaylistcollection:: importwiedergabe-Methode</span><span class="sxs-lookup"><span data-stu-id="c8888-107">IWMPPlaylistCollection::importPlaylist method</span></span>

<span data-ttu-id="c8888-108">Die **importwiedergabe** -Methode fügt der Bibliothek eine statische Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="c8888-108">The **importPlaylist** method adds a static playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8888-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8888-109">Syntax</span></span>


```CSharp
public IWMPPlaylist importPlaylist(
  IWMPPlaylist pItem
);
```


```VB

Public Function importPlaylist( _
  ByVal pItem As IWMPPlaylist _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.importPlaylist
```





## <a name="parameters"></a><span data-ttu-id="c8888-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8888-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8888-111">*pitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8888-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8888-112">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die Wiedergabeliste, die von dieser Methode hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c8888-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8888-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8888-113">Return value</span></span>

<span data-ttu-id="c8888-114">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die hinzugefügte Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="c8888-114">A **WMPLib.IWMPPlaylist** interface for the added playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8888-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8888-115">Remarks</span></span>

<span data-ttu-id="c8888-116">Wiedergabelisten, die keine Medienelemente enthalten, können der Bibliothek nicht mithilfe dieser Methode hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c8888-116">Playlists that do not contain any media items cannot be added to the library by using this method.</span></span> <span data-ttu-id="c8888-117">Verwenden Sie die **newwiedergabe** -Methode, um eine leere Wiedergabeliste in der Bibliothek zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c8888-117">To create an empty playlist in the library, use the **newPlaylist** method.</span></span> <span data-ttu-id="c8888-118">Anschließend können Sie die resultierende Wiedergabeliste mit den Medien Elementen füllen, indem Sie **iwmpwiedergabe. appendItem** oder **iwmpwiedergabe. InsertItem** verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8888-118">You can then fill the resulting playlist with media items by using **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="c8888-119">Wenn Sie diese Methode an eine automatische Wiedergabeliste übergeben, wird die Abfrage einmal ausgeführt, und das Ergebnis wird der Bibliothek als statische Wiedergabeliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c8888-119">If you pass this method an auto playlist, the query is executed once and the result is added to the library as a static playlist.</span></span> <span data-ttu-id="c8888-120">Wenn Sie der Bibliothek eine automatische Wiedergabeliste hinzufügen und das automatische Verhalten beibehalten möchten, verwenden Sie **iwmpmediacollection. Add**.</span><span class="sxs-lookup"><span data-stu-id="c8888-120">To add an auto playlist to the library and preserve its automatic behavior, use **IWMPMediaCollection.add**.</span></span> <span data-ttu-id="c8888-121">Weitere Informationen finden Sie unter [statische und automatische Wiedergabelisten](static-and-auto-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="c8888-121">For more information, see [Static and Auto Playlists](static-and-auto-playlists.md).</span></span>

<span data-ttu-id="c8888-122">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="c8888-122">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c8888-123">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c8888-123">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8888-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8888-124">Requirements</span></span>



| <span data-ttu-id="c8888-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8888-125">Requirement</span></span> | <span data-ttu-id="c8888-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c8888-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8888-127">Version</span><span class="sxs-lookup"><span data-stu-id="c8888-127">Version</span></span><br/>   | <span data-ttu-id="c8888-128">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c8888-128">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="c8888-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8888-129">Namespace</span></span><br/> | <span data-ttu-id="c8888-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c8888-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c8888-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="c8888-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c8888-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c8888-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8888-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8888-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8888-134">**Iwmpmediacollection. Add (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8888-134">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8888-135">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8888-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8888-136">**Iwmpwiedergabe. appendItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8888-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8888-137">**Iwmpwiedergabe. InsertItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8888-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8888-138">**Iwmpplaylistcollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8888-138">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8888-139">**Iwmpplaylistcollection. newwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8888-139">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





