---
title: AxWindowsMediaPlayer. currentwiedergabe (Eigenschaft)
description: Die currentwiedergabe-Eigenschaft ruft die aktuelle iwmpwiedergabe-Schnittstelle ab, die eine einfache Möglichkeit zum organisieren und Bearbeiten von Medien Elementen in einer Liste bietet, oder legt diese fest.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- currentwiedergabe-Eigenschaft, Windows-Media Player
- currentwiedergabe-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, currentwiedergabe-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368636"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a><span data-ttu-id="2a720-106">AxWindowsMediaPlayer. currentwiedergabe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2a720-106">AxWindowsMediaPlayer.currentPlaylist property</span></span>

<span data-ttu-id="2a720-107">Die currentwiedergabe-Eigenschaft ruft die aktuelle **iwmpwiedergabe** -Schnittstelle ab, die eine einfache Möglichkeit zum organisieren und Bearbeiten von Medien Elementen in einer Liste bietet, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="2a720-107">The currentPlaylist property gets or sets the current **IWMPPlaylist** interface that provides an easy way to organize and manipulate media items in a list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a720-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a720-108">Syntax</span></span>


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="2a720-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2a720-109">Property value</span></span>

<span data-ttu-id="2a720-110">Die WMPLib. iwmpwiedergabe-Schnittstelle, die Zugriff auf die aktuelle Wiedergabeliste bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2a720-110">The WMPLib.IWMPPlaylist interface that provides access to the current playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a720-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a720-111">Remarks</span></span>

<span data-ttu-id="2a720-112">, Wenn die iwmpsettings. AutoStart-Eigenschaft (auch über AxWindowsMediaPlayer. Settings aufgerufen wird.**Autostart**) ist "true", wenn Sie " **currentwiedergabe**" festlegen, beginnt die Wiedergabe automatisch.</span><span class="sxs-lookup"><span data-stu-id="2a720-112">If the IWMPSettings.autoStart property (also accessed via AxWindowsMediaPlayer.settings.**autoStart**) is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="2a720-113">Diese Eigenschaft nimmt eine iwmpwiedergabe-Schnittstelle an, die auf verschiedene Weise abgerufen werden kann, z. b. durch das erhalten des Werts aus dem *iwmpplaylistarray*. **Element** oder *iwmpplaylistcollection*. **newwiedergabe** -Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2a720-113">This property takes an IWMPPlaylist interface, which can be acquired in several ways, such as by getting the value from the *IWMPPlaylistArray*.**Item** or *IWMPPlaylistCollection*.**newPlaylist** properties.</span></span> <span data-ttu-id="2a720-114">Wenn Sie ein **Wiedergabe** Listenelement mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest, oder verwenden Sie AxWindowsMediaPlayer. **newwiedergabe**.</span><span class="sxs-lookup"><span data-stu-id="2a720-114">To load a **playlist** item using a file name, set the URL property or use AxWindowsMediaPlayer.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="2a720-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a720-115">Examples</span></span>

<span data-ttu-id="2a720-116">Im folgenden Beispiel wird die erste Wiedergabeliste in der Bibliothek abgerufen und die currentwiedergabe-Eigenschaft verwendet, um die abgerufene Wiedergabeliste als aktuelle Wiedergabeliste festzulegen und deren Namen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2a720-116">The following example retrieves the first playlist in the library and uses the currentPlaylist property to set the retrieved playlist as the current playlist, and display its name.</span></span> <span data-ttu-id="2a720-117">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2a720-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a><span data-ttu-id="2a720-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a720-118">Requirements</span></span>



| <span data-ttu-id="2a720-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a720-119">Requirement</span></span> | <span data-ttu-id="2a720-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2a720-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a720-121">Version</span><span class="sxs-lookup"><span data-stu-id="2a720-121">Version</span></span><br/>   | <span data-ttu-id="2a720-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2a720-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2a720-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a720-123">Namespace</span></span><br/> | <span data-ttu-id="2a720-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2a720-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2a720-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="2a720-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2a720-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2a720-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a720-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a720-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a720-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2a720-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a720-129">**AxWindowsMediaPlayer. newwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2a720-129">**AxWindowsMediaPlayer.newPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="2a720-130">**AxWindowsMediaPlayer. Settings (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2a720-130">**AxWindowsMediaPlayer.settings (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a720-131">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2a720-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a720-132">**Iwmpplaylistarray. Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2a720-132">**IWMPPlaylistArray.Item (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a720-133">**Iwmpplaylistcollection. newwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2a720-133">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2a720-134">**Iwmpsettings. Autostart (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2a720-134">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





