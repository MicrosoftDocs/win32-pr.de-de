---
title: Iwmpmedia SourceURL (Eigenschaft)
description: Die SourceUrl-Eigenschaft ruft die URL des Medien Elements ab.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- SourceURL-Eigenschaften Fenster Media Player
- SourceURL-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, SourceURL (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372409"
---
# <a name="iwmpmediasourceurl-property"></a><span data-ttu-id="e9a7e-106">Iwmpmedia:: SourceURL (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e9a7e-106">IWMPMedia::sourceURL property</span></span>

<span data-ttu-id="e9a7e-107">Die **SourceUrl** -Eigenschaft ruft die URL des Medien Elements ab.</span><span class="sxs-lookup"><span data-stu-id="e9a7e-107">The **sourceURL** property gets the URL of the media item.</span></span>

<span data-ttu-id="e9a7e-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e9a7e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a7e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9a7e-109">Syntax</span></span>


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="e9a7e-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e9a7e-110">Property value</span></span>

<span data-ttu-id="e9a7e-111">Ein **System. String** -Wert, der die Quell-URL ist.</span><span class="sxs-lookup"><span data-stu-id="e9a7e-111">A **System.String** that is the source URL.</span></span>

## <a name="examples"></a><span data-ttu-id="e9a7e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9a7e-112">Examples</span></span>

<span data-ttu-id="e9a7e-113">Im folgenden Beispiel wird **SourceUrl** verwendet, um die URL des ersten Medien Elements in der Wiedergabeliste "alle Musik" abzurufen. die URL des Medien Elements wird dann der Eigenschaft "Player Object URL" zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e9a7e-113">The following example uses **sourceURL** to retrieve the URL of the first media item in the "All Music" playlist; the URL of the media item is then assigned to the player object URL property.</span></span> <span data-ttu-id="e9a7e-114">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e9a7e-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="e9a7e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9a7e-115">Requirements</span></span>



| <span data-ttu-id="e9a7e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9a7e-116">Requirement</span></span> | <span data-ttu-id="e9a7e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e9a7e-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a7e-118">Version</span><span class="sxs-lookup"><span data-stu-id="e9a7e-118">Version</span></span><br/>   | <span data-ttu-id="e9a7e-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e9a7e-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e9a7e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e9a7e-120">Namespace</span></span><br/> | <span data-ttu-id="e9a7e-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e9a7e-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e9a7e-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="e9a7e-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e9a7e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e9a7e-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a7e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9a7e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a7e-125">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e9a7e-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





