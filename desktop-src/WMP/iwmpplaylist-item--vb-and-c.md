---
title: Iwmpwiedergabe. Item (VB und C)
description: Die Item-Eigenschaft (die get \_ Item-Methode in C \) Ruft eine Schnittstelle zum Medien Element am angegebenen Index ab.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- Iwmpwiedergabe. Item (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364413"
---
# <a name="iwmpplaylistitem-vb-and-c"></a><span data-ttu-id="756cf-104">Iwmpwiedergabe. Item (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="756cf-104">IWMPPlaylist.Item (VB and C#)</span></span>

<span data-ttu-id="756cf-105">Die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) Ruft eine Schnittstelle zum Medien Element am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="756cf-105">The **Item** property (the **get\_Item** method in C#) gets an interface to the media item at the specified index.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a><span data-ttu-id="756cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="756cf-106">Parameters</span></span>

<span data-ttu-id="756cf-107">*Lindex*</span><span class="sxs-lookup"><span data-stu-id="756cf-107">*lIndex*</span></span>

<span data-ttu-id="756cf-108">Ein **System. Int32** -Wert, der den Index des Medien Elements in der Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="756cf-108">A **System.Int32** that is the index of the media item in the playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="756cf-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="756cf-109">Property Value</span></span>

<span data-ttu-id="756cf-110">Eine **WMPLib. iwmpmedia** -Schnittstelle, die Zugriff auf das Medien Element am angegebenen Index bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="756cf-110">An **WMPLib.IWMPMedia** interface that provides access to the media item at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="756cf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="756cf-111">Remarks</span></span>

<span data-ttu-id="756cf-112">**Iwmpwiedergabe. Item** ist eine schreibgeschützte Eigenschaft in Visual Basic, die einen-Parameter annimmt, während in c# als **iwmpwiedergabe. get- \_ Element** Methode bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="756cf-112">**IWMPPlaylist.Item** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_Item** method.</span></span>

## <a name="examples"></a><span data-ttu-id="756cf-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="756cf-113">Examples</span></span>

<span data-ttu-id="756cf-114">Im folgenden Beispiel wird die **Item** -Eigenschaft (die **get \_ Item** -Methode in c#) zum Abrufen eines Medien Elements aus einer Wiedergabeliste basierend auf einer Benutzer Auswahl verwendet.</span><span class="sxs-lookup"><span data-stu-id="756cf-114">The following example uses the **Item** property (the **get\_Item** method in C#) to retrieve a media item from a playlist based on a user selection.</span></span> <span data-ttu-id="756cf-115">Ein Listenfeld mit dem Namen weblist wurde erstellt und mit den Titeln der Wiedergabeliste mit dem Namen audioplaylist gefüllt.</span><span class="sxs-lookup"><span data-stu-id="756cf-115">A list box was created with the name weblist, and filled with the titles from the playlist called audioPlaylist.</span></span> <span data-ttu-id="756cf-116">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="756cf-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a><span data-ttu-id="756cf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="756cf-117">Requirements</span></span>



| <span data-ttu-id="756cf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="756cf-118">Requirement</span></span> | <span data-ttu-id="756cf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="756cf-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="756cf-120">Version</span><span class="sxs-lookup"><span data-stu-id="756cf-120">Version</span></span><br/>   | <span data-ttu-id="756cf-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="756cf-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="756cf-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="756cf-122">Namespace</span></span><br/> | <span data-ttu-id="756cf-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="756cf-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="756cf-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="756cf-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="756cf-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="756cf-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="756cf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="756cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756cf-127">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="756cf-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="756cf-128">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="756cf-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="756cf-129">**Iwmpwiedergabe. InsertItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="756cf-129">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="756cf-130">**Iwmpwiedergabe. RemoveItem (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="756cf-130">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="756cf-131">**IWMPSettings2. mediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="756cf-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="756cf-132">**IWMPSettings2. requestmediaaccessrights (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="756cf-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





