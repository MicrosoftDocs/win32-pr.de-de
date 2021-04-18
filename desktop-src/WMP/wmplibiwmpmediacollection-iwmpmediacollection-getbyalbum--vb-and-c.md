---
title: Iwmpmediacollection getbyalbum-Methode
description: Die getbyalbum-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die den Zugriff auf Medienelemente aus dem angegebenen Album ermöglicht.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- getbyalbum-Methode, Windows-Media Player
- getbyalbum-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection Interface, Windows Media Player, getbyalbum-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365837"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a><span data-ttu-id="c8b52-106">Iwmpmediacollection:: getbyalbum-Methode</span><span class="sxs-lookup"><span data-stu-id="c8b52-106">IWMPMediaCollection::getByAlbum method</span></span>

<span data-ttu-id="c8b52-107">Die **getbyalbum** -Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente aus dem angegebenen Album ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c8b52-107">The **getByAlbum** method returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b52-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8b52-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a><span data-ttu-id="c8b52-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8b52-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8b52-110">*bstrinalbum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8b52-110">*bstrAlbum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8b52-111">Die **System. String** , die den Titel des Albums ist.</span><span class="sxs-lookup"><span data-stu-id="c8b52-111">The **System.String** that is the title of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8b52-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8b52-112">Return value</span></span>

<span data-ttu-id="c8b52-113">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufenen Medienelemente.</span><span class="sxs-lookup"><span data-stu-id="c8b52-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8b52-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8b52-114">Remarks</span></span>

<span data-ttu-id="c8b52-115">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="c8b52-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="c8b52-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c8b52-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c8b52-117">Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der **getbyalbum** -Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8b52-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAlbum** method depends on which of those two ways you use.</span></span> <span data-ttu-id="c8b52-118">Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die **getbyalbum** -Methode alle Medienelemente in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="c8b52-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAlbum** method returns all the media items in the library.</span></span> <span data-ttu-id="c8b52-119">Wenn Sie jedoch die Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, gibt die **getbyalbum** -Methode nur die Audioelemente in der Bibliothek zurück, die zum angegebenen Album gehören.</span><span class="sxs-lookup"><span data-stu-id="c8b52-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAlbum** method returns only the audio items in the library that belong to the specified album.</span></span>

## <a name="examples"></a><span data-ttu-id="c8b52-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8b52-120">Examples</span></span>

<span data-ttu-id="c8b52-121">Im folgenden Beispiel wird **getbyalbum** verwendet, um eine Wiedergabeliste von Medien Elementen zu erstellen, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="c8b52-121">The following example uses **getByAlbum** to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="c8b52-122">Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Album in einem Textfeld.</span><span class="sxs-lookup"><span data-stu-id="c8b52-122">The playlist contains items with the album specified by the user in a text box.</span></span> <span data-ttu-id="c8b52-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c8b52-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c8b52-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8b52-124">Requirements</span></span>



| <span data-ttu-id="c8b52-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8b52-125">Requirement</span></span> | <span data-ttu-id="c8b52-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c8b52-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b52-127">Version</span><span class="sxs-lookup"><span data-stu-id="c8b52-127">Version</span></span><br/>   | <span data-ttu-id="c8b52-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="c8b52-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c8b52-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8b52-129">Namespace</span></span><br/> | <span data-ttu-id="c8b52-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c8b52-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c8b52-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="c8b52-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c8b52-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c8b52-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b52-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8b52-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b52-134">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8b52-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c8b52-135">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="c8b52-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





