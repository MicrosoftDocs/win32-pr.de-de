---
title: Iwmpmediacollection getbygenre-Methode
description: Die getbygenre-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die den Zugriff auf Medienelemente des angegebenen Genres ermöglicht.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- getbygenre-Methode, Windows-Media Player
- getbygenre-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection Interface, Windows Media Player, getbygenre-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359802"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a><span data-ttu-id="ef8bf-106">Iwmpmediacollection:: getbygenre-Methode</span><span class="sxs-lookup"><span data-stu-id="ef8bf-106">IWMPMediaCollection::getByGenre method</span></span>

<span data-ttu-id="ef8bf-107">Die- `getByGenre` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente des angegebenen Genres ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-107">The `getByGenre` method returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8bf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef8bf-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a><span data-ttu-id="ef8bf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef8bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef8bf-110">*bstringenre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef8bf-110">*bstrGenre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef8bf-111">Der **System. String** -Wert, der der Name des Genres ist.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-111">The **System.String** that is the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef8bf-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef8bf-112">Return value</span></span>

<span data-ttu-id="ef8bf-113">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufenen Medienelemente.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef8bf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef8bf-114">Remarks</span></span>

<span data-ttu-id="ef8bf-115">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="ef8bf-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ef8bf-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ef8bf-117">Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der- `getByGenre` Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByGenre` method depends on which of those two ways you use.</span></span> <span data-ttu-id="ef8bf-118">Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die- `getByGenre` Methode alle Medienelemente in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByGenre` method returns all the media items in the library.</span></span> <span data-ttu-id="ef8bf-119">Wenn Sie jedoch die-Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, `getByGenre` gibt die-Methode nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und den angegebenen Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByGenre` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="ef8bf-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef8bf-120">Examples</span></span>

<span data-ttu-id="ef8bf-121">Im folgenden Beispiel wird verwendet `getByGenre` , um eine Wiedergabeliste von Medien Elementen abzurufen, wenn der Benutzer auf eine Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-121">The following example uses `getByGenre` to retrieve a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="ef8bf-122">Die Wiedergabeliste enthält Elemente mit dem vom Benutzer angegebenen Genre in einem Textfeld.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-122">The playlist contains items with the genre specified by the user in a text box.</span></span> <span data-ttu-id="ef8bf-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ef8bf-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="ef8bf-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef8bf-124">Requirements</span></span>



| <span data-ttu-id="ef8bf-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef8bf-125">Requirement</span></span> | <span data-ttu-id="ef8bf-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ef8bf-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8bf-127">Version</span><span class="sxs-lookup"><span data-stu-id="ef8bf-127">Version</span></span><br/>   | <span data-ttu-id="ef8bf-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ef8bf-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ef8bf-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ef8bf-129">Namespace</span></span><br/> | <span data-ttu-id="ef8bf-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ef8bf-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ef8bf-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="ef8bf-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ef8bf-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ef8bf-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef8bf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef8bf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8bf-134">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ef8bf-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ef8bf-135">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ef8bf-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





