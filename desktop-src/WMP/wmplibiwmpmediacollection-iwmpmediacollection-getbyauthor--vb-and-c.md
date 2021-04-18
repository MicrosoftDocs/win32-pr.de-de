---
title: Iwmpmediacollection getbyauthor-Methode
description: Die getbyauthor-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die den Zugriff auf die Medienelemente durch den angegebenen Autor ermöglicht.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- getbyauthor-Methode, Windows-Media Player
- getbyauthor-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, getbyauthor-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e594de010a65c15088e2a31a3ccbac2ac5a1fc6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358149"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a><span data-ttu-id="42a32-106">Iwmpmediacollection:: getbyauthor-Methode</span><span class="sxs-lookup"><span data-stu-id="42a32-106">IWMPMediaCollection::getByAuthor method</span></span>

<span data-ttu-id="42a32-107">Die- `getByAuthor` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf die Medienelemente durch den angegebenen Autor ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="42a32-107">The `getByAuthor` method returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a32-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a32-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a><span data-ttu-id="42a32-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="42a32-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a32-110">*bstrauauthor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42a32-110">*bstrAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a32-111">Die **System. String** , die den Namen des Autors ist.</span><span class="sxs-lookup"><span data-stu-id="42a32-111">The **System.String** that is the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a32-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="42a32-112">Return value</span></span>

<span data-ttu-id="42a32-113">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufenen Medienelemente.</span><span class="sxs-lookup"><span data-stu-id="42a32-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a32-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a32-114">Remarks</span></span>

<span data-ttu-id="42a32-115">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="42a32-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="42a32-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="42a32-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="42a32-117">Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der- `getByAuthor` Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="42a32-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByAuthor` method depends on which of those two ways you use.</span></span> <span data-ttu-id="42a32-118">Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die- `getByAuthor` Methode alle Medienelemente in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="42a32-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByAuthor` method returns all the media items in the library.</span></span> <span data-ttu-id="42a32-119">Wenn Sie jedoch die-Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, `getByAuthor` gibt die-Methode nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und den angegebenen Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="42a32-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByAuthor` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="42a32-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42a32-120">Examples</span></span>

<span data-ttu-id="42a32-121">Im folgenden Beispiel wird verwendet `getByAuthor` , um eine Wiedergabeliste von Medien Elementen zu erstellen, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="42a32-121">The following example uses `getByAuthor` to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="42a32-122">Die Wiedergabeliste enthält Elemente, die mit dem Namen des Autors übereinstimmen, der vom Benutzer in einem Textfeld angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42a32-122">The playlist contains items matching the author's name specified by the user in a text box.</span></span> <span data-ttu-id="42a32-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="42a32-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="42a32-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="42a32-124">Requirements</span></span>



| <span data-ttu-id="42a32-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a32-125">Requirement</span></span> | <span data-ttu-id="42a32-126">Wert</span><span class="sxs-lookup"><span data-stu-id="42a32-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a32-127">Version</span><span class="sxs-lookup"><span data-stu-id="42a32-127">Version</span></span><br/>   | <span data-ttu-id="42a32-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="42a32-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="42a32-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="42a32-129">Namespace</span></span><br/> | <span data-ttu-id="42a32-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="42a32-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="42a32-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="42a32-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="42a32-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="42a32-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a32-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42a32-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a32-134">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="42a32-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="42a32-135">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="42a32-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





