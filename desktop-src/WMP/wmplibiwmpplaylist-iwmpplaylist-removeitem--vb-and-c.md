---
title: Iwmpwiedergabe RemoveItem-Methode
description: Mit der RemoveItem-Methode wird das angegebene Medien Element aus der Wiedergabeliste entfernt.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- RemoveItem-Methode, Windows-Media Player
- RemoveItem-Methode, Windows Media Player, iwmpwiedergabe-Schnittstelle
- Iwmpwiedergabe Interface, Windows Media Player, RemoveItem-Methode
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364861"
---
# <a name="iwmpplaylistremoveitem-method"></a><span data-ttu-id="51450-106">Iwmpwiedergabe:: RemoveItem-Methode</span><span class="sxs-lookup"><span data-stu-id="51450-106">IWMPPlaylist::removeItem method</span></span>

<span data-ttu-id="51450-107">Mit der **RemoveItem** -Methode wird das angegebene Medien Element aus der Wiedergabeliste entfernt.</span><span class="sxs-lookup"><span data-stu-id="51450-107">The **removeItem** method removes the specified media item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="51450-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="51450-108">Syntax</span></span>


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a><span data-ttu-id="51450-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="51450-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51450-110">*piwmpmedia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51450-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51450-111">Eine **WMPLib. iwmpmedia** -Schnittstelle, die das Medien Element darstellt, das aus der Wiedergabeliste entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="51450-111">A **WMPLib.IWMPMedia** interface that represents the media item to remove from the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51450-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51450-112">Return value</span></span>

<span data-ttu-id="51450-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="51450-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51450-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51450-114">Remarks</span></span>

<span data-ttu-id="51450-115">Wenn das entfernte Element die aktuell Wiedergabe ist, wird die Wiedergabe angehalten, und das nächste Element in der Wiedergabeliste wird zum aktuellen Element.</span><span class="sxs-lookup"><span data-stu-id="51450-115">If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.</span></span>

<span data-ttu-id="51450-116">Wenn kein nächstes Element vorhanden ist, wird das vorherige Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="51450-116">If there is no next item, the previous item is used.</span></span> <span data-ttu-id="51450-117">Wenn keine anderen Elemente vorhanden sind, gibt die **AxWindowsMediaPlayer. currentMedia** -Eigenschaft **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="51450-117">If there are no other items, then the **AxWindowsMediaPlayer.currentMedia** property will return **NULL**.</span></span>

<span data-ttu-id="51450-118">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="51450-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="51450-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="51450-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51450-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51450-120">Requirements</span></span>



| <span data-ttu-id="51450-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51450-121">Requirement</span></span> | <span data-ttu-id="51450-122">Wert</span><span class="sxs-lookup"><span data-stu-id="51450-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51450-123">Version</span><span class="sxs-lookup"><span data-stu-id="51450-123">Version</span></span><br/>   | <span data-ttu-id="51450-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="51450-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="51450-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="51450-125">Namespace</span></span><br/> | <span data-ttu-id="51450-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="51450-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="51450-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="51450-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="51450-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="51450-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51450-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51450-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51450-130">**AxWindowsMediaPlayer. currentMedia (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51450-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51450-131">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51450-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51450-132">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51450-132">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51450-133">**Iwmpwiedergabe. InsertItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51450-133">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51450-134">**Iwmpwiedergabe. Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51450-134">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51450-135">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51450-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="51450-136">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="51450-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





