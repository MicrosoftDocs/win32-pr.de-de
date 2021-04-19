---
title: "' Iwmpmediacollection ' getByName-Methode"
description: Die getByName-Methode gibt eine iwmpwiedergabe-Schnittstelle zurück, die den Zugriff auf Medienelemente mit dem angegebenen Namen ermöglicht.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- getByName-Methode, Windows-Media Player
- getByName-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection Interface, Windows Media Player, getByName-Methode
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367197"
---
# <a name="iwmpmediacollectiongetbyname-method"></a><span data-ttu-id="19f05-106">Iwmpmediacollection:: getByName-Methode</span><span class="sxs-lookup"><span data-stu-id="19f05-106">IWMPMediaCollection::getByName method</span></span>

<span data-ttu-id="19f05-107">Die- `getByName` Methode gibt eine **iwmpwiedergabe** -Schnittstelle zurück, die den Zugriff auf Medienelemente mit dem angegebenen Namen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="19f05-107">The `getByName` method returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f05-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="19f05-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="19f05-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="19f05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f05-110">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19f05-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19f05-111">Die **System. String** mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="19f05-111">The **System.String** that is the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f05-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19f05-112">Return value</span></span>

<span data-ttu-id="19f05-113">Eine **WMPLib. iwmpwiedergabe** -Schnittstelle für die abgerufenen Medienelemente.</span><span class="sxs-lookup"><span data-stu-id="19f05-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="19f05-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19f05-114">Remarks</span></span>

<span data-ttu-id="19f05-115">Vor dem Aufrufen dieser Methode müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="19f05-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="19f05-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="19f05-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="19f05-117">Es gibt zwei Möglichkeiten, wie Sie eine **iwmpmediacollection** -Schnittstelle abrufen können, und das Verhalten der- `getByName` Methode hängt davon ab, welche dieser beiden Methoden Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="19f05-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByName` method depends on which of those two ways you use.</span></span> <span data-ttu-id="19f05-118">Wenn Sie die Schnittstelle abrufen, indem Sie [AxWindowsMediaPlayer. mediacollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)aufrufen, gibt die- `getByName` Methode alle Medienelemente in der Bibliothek zurück.</span><span class="sxs-lookup"><span data-stu-id="19f05-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByName` method returns all the media items in the library.</span></span> <span data-ttu-id="19f05-119">Wenn Sie jedoch die-Schnittstelle abrufen, indem Sie [iwmplibrary. mediacollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)aufrufen, `getByName` gibt die-Methode nur die Audioelemente in der Bibliothek zurück, die über das angegebene Attribut und den angegebenen Wert verfügen.</span><span class="sxs-lookup"><span data-stu-id="19f05-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByName` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="19f05-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19f05-120">Examples</span></span>

<span data-ttu-id="19f05-121">Im folgenden Beispiel wird verwendet `getByName` , um drei Elemente aus der Bibliothek abzurufen.</span><span class="sxs-lookup"><span data-stu-id="19f05-121">The following example uses `getByName` to retrieve three items from the library.</span></span> <span data-ttu-id="19f05-122">Jedes Element wird dann an die aktuelle Wiedergabeliste angehängt.</span><span class="sxs-lookup"><span data-stu-id="19f05-122">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="19f05-123">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="19f05-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a><span data-ttu-id="19f05-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19f05-124">Requirements</span></span>



| <span data-ttu-id="19f05-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19f05-125">Requirement</span></span> | <span data-ttu-id="19f05-126">Wert</span><span class="sxs-lookup"><span data-stu-id="19f05-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f05-127">Version</span><span class="sxs-lookup"><span data-stu-id="19f05-127">Version</span></span><br/>   | <span data-ttu-id="19f05-128">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="19f05-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="19f05-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="19f05-129">Namespace</span></span><br/> | <span data-ttu-id="19f05-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="19f05-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="19f05-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="19f05-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="19f05-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="19f05-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19f05-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19f05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f05-134">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="19f05-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="19f05-135">**Iwmpwiedergabe-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="19f05-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





