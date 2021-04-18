---
title: Iwmpwiedergabe appendItem-Methode
description: Mit der appendItem-Methode wird am Ende einer Wiedergabeliste ein Medien Element hinzugefügt.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- appendItem-Methode, Windows Media Player
- appendItem-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, appendItem-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354753"
---
# <a name="iwmpplaylistappenditem-method"></a><span data-ttu-id="ed3ff-106">Iwmpwiedergabe:: appendItem-Methode</span><span class="sxs-lookup"><span data-stu-id="ed3ff-106">IWMPPlaylist::appendItem method</span></span>

<span data-ttu-id="ed3ff-107">Mit der **appendItem** -Methode wird am Ende einer Wiedergabeliste ein Medien Element hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-107">The **appendItem** method adds a media item to the end of a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed3ff-108">Syntax</span></span>


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a><span data-ttu-id="ed3ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed3ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed3ff-110">*piwmpmedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed3ff-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed3ff-111">Eine **WMPLib. iwmpmedia** -Schnittstelle, die das anzufügende Medien Element darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-111">An **WMPLib.IWMPMedia** interface that represents the media item to be appended.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed3ff-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed3ff-112">Return value</span></span>

<span data-ttu-id="ed3ff-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed3ff-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed3ff-114">Remarks</span></span>

<span data-ttu-id="ed3ff-115">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-115">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="ed3ff-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ed3ff-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ed3ff-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed3ff-117">Examples</span></span>

<span data-ttu-id="ed3ff-118">Im folgenden Beispiel wird **appendItem** verwendet, um der Wiedergabeliste das aktuelle Medien Element mit dem Namen "threelist" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-118">The following example uses **appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="ed3ff-119">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ed3ff-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a><span data-ttu-id="ed3ff-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed3ff-120">Requirements</span></span>



| <span data-ttu-id="ed3ff-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed3ff-121">Requirement</span></span> | <span data-ttu-id="ed3ff-122">Wert</span><span class="sxs-lookup"><span data-stu-id="ed3ff-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3ff-123">Version</span><span class="sxs-lookup"><span data-stu-id="ed3ff-123">Version</span></span><br/>   | <span data-ttu-id="ed3ff-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ed3ff-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ed3ff-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed3ff-125">Namespace</span></span><br/> | <span data-ttu-id="ed3ff-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ed3ff-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ed3ff-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="ed3ff-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ed3ff-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ed3ff-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed3ff-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed3ff-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3ff-130">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ed3ff-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ed3ff-131">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ed3ff-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





