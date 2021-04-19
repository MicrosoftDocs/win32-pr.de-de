---
title: AxWindowsMediaPlayer. newwiedergabe-Methode
description: Die newwiedergabe-Methode gibt eine iwmpwiedergabe-Schnittstelle für eine neue Wiedergabeliste zurück.
ms.assetid: caee8ee5-6201-474d-a4cb-80e574f84f0b
keywords:
- newwiedergabe-Methode, Windows-Media Player
- newwiedergabe-Methode, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, newwiedergabe-Methode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc82be7aae37b4c1334b79f84e9d607b4f73cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370205"
---
# <a name="axwindowsmediaplayernewplaylist-method"></a><span data-ttu-id="98566-106">AxWindowsMediaPlayer. newwiedergabe-Methode</span><span class="sxs-lookup"><span data-stu-id="98566-106">AxWindowsMediaPlayer.newPlaylist method</span></span>

<span data-ttu-id="98566-107">Die newwiedergabe-Methode gibt eine iwmpwiedergabe-Schnittstelle für eine neue Wiedergabeliste zurück.</span><span class="sxs-lookup"><span data-stu-id="98566-107">The newPlaylist method returns an IWMPPlaylist interface for a new playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="98566-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="98566-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName,
  System.String bstrURL
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String, _
  ByVal bstrURL As System.String _
) As IWMPPlaylist
```





## <a name="parameters"></a><span data-ttu-id="98566-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="98566-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98566-110">*bstrName*</span><span class="sxs-lookup"><span data-stu-id="98566-110">*bstrName*</span></span> 
</dt> <dd>

<span data-ttu-id="98566-111">Die **System. String** -Wert, der der Name der neuen Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="98566-111">The **System.String** that is the name of the new playlist.</span></span>

</dd> <dt>

<span data-ttu-id="98566-112">*bstrURL*</span><span class="sxs-lookup"><span data-stu-id="98566-112">*bstrURL*</span></span> 
</dt> <dd>

<span data-ttu-id="98566-113">Die **System. String** -URL, die die URL der Windows Media Metadatei-Wiedergabeliste ist, die zum Initialisieren der neuen Wiedergabeliste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="98566-113">The **System.String** that is the URL of the Windows Media metafile playlist that is used to initialize the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98566-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98566-114">Return value</span></span>

<span data-ttu-id="98566-115">Eine WMPLib. iwmpwiedergabe-Schnittstelle, die die neu erstellte Wiedergabeliste darstellt.</span><span class="sxs-lookup"><span data-stu-id="98566-115">A WMPLib.IWMPPlaylist interface that represents the newly created playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="98566-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98566-116">Remarks</span></span>

<span data-ttu-id="98566-117">Wenn der *bstrinurl* -Parameter eine NULL-Zeichenfolge oder eine Zeichenfolge der Länge 0 ("") ist, erstellt diese Methode eine leere **Wiedergabeliste**.</span><span class="sxs-lookup"><span data-stu-id="98566-117">If the *bstrURL* parameter is a null or zero-length string (""), this method creates an empty **playlist**.</span></span> <span data-ttu-id="98566-118">Wenn der *bstrinname* -Parameter eine Zeichenfolge der Länge 0 ("") ist, wendet diese Methode den aktuellen metadateinamen an.</span><span class="sxs-lookup"><span data-stu-id="98566-118">If the *bstrName* parameter is a zero-length string (""), this method applies the current metafile name.</span></span>

<span data-ttu-id="98566-119">Die neue Wiedergabeliste, die mit dieser Methode erstellt wurde, wird nicht der Bibliothek hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="98566-119">The new playlist created with this method is not added to the library.</span></span> <span data-ttu-id="98566-120">Um der Bibliothek eine neue Wiedergabeliste hinzuzufügen, verwenden Sie iwmpplaylistcollection. **importwiedergabe Liste** oder iwmpplaylistcollection. **newwiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="98566-120">To add a new playlist to the library, use IWMPPlaylistCollection.**importPlaylist** or IWMPPlaylistCollection.**newPlaylist**.</span></span> <span data-ttu-id="98566-121">Alle führenden oder nachfolgenden Leerzeichen im Wiedergabelisten Namen werden automatisch entfernt, wenn Sie der Bibliothek hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="98566-121">Any leading or trailing spaces in the playlist name are automatically removed when it is added to the library.</span></span>

<span data-ttu-id="98566-122">Da die Bibliothek mehrere Wiedergabelisten mit dem gleichen Namen zulässt, sollten Sie überprüfen, ob eine Wiedergabeliste mit einem bestimmten Namen vorhanden ist, bevor Sie einen neuen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="98566-122">Because the library allows multiple playlists with the same name, you may want to check for the presence of a playlist with a given name before adding a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="98566-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98566-123">Requirements</span></span>



| <span data-ttu-id="98566-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98566-124">Requirement</span></span> | <span data-ttu-id="98566-125">Wert</span><span class="sxs-lookup"><span data-stu-id="98566-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98566-126">Version</span><span class="sxs-lookup"><span data-stu-id="98566-126">Version</span></span><br/>   | <span data-ttu-id="98566-127">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="98566-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="98566-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="98566-128">Namespace</span></span><br/> | <span data-ttu-id="98566-129">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="98566-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="98566-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="98566-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="98566-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="98566-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98566-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98566-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98566-133">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="98566-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98566-134">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="98566-134">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98566-135">**Iwmpplaylistcollection. importwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="98566-135">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="98566-136">**Iwmpplaylistcollection. newwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="98566-136">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> </dl>

 

 





