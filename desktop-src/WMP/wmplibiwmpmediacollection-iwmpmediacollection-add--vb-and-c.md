---
title: Iwmpmediacollection-Methode hinzufügen
description: Die Add-Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu. | Iwmpmediacollection-Methode hinzufügen
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Hinzufügen von Methoden Fenster Media Player
- Add-Methode, Windows Media Player, iwmpmediacollection-Schnittstelle
- Iwmpmediacollection-Schnittstelle, Windows Media Player, Methode hinzufügen
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370509"
---
# <a name="iwmpmediacollectionadd-method"></a><span data-ttu-id="af24b-107">Iwmpmediacollection:: Add-Methode</span><span class="sxs-lookup"><span data-stu-id="af24b-107">IWMPMediaCollection::add method</span></span>

<span data-ttu-id="af24b-108">Die **Add** -Methode fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="af24b-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="af24b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="af24b-109">Syntax</span></span>


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a><span data-ttu-id="af24b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="af24b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af24b-111">*bstrinurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af24b-111">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af24b-112">Eine **System. String** -URL, die den Speicherort des Medien Elements oder der Wiedergabeliste angibt.</span><span class="sxs-lookup"><span data-stu-id="af24b-112">A **System.String** that is the URL that specifies the location of the media item or playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af24b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af24b-113">Return value</span></span>

<span data-ttu-id="af24b-114">Die **WMPLib. iwmpmedia** -Schnittstelle für das hinzugefügte Element oder Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="af24b-114">The **WMPLib.IWMPMedia** interface for the added item or playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="af24b-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af24b-115">Remarks</span></span>

<span data-ttu-id="af24b-116">Diese Methode lädt ein vorhandenes Medien Element oder eine vorhandene Wiedergabeliste in die Bibliothek, sofern ein Pfad angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="af24b-116">This method loads an existing media item or playlist into the library, given a path.</span></span> <span data-ttu-id="af24b-117">Diese Methode verschiebt oder ändert die Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="af24b-117">This method does not move or change the file.</span></span> <span data-ttu-id="af24b-118">Bei dieser Methode tritt ein Fehler auf, wenn ein ungültiger lokaler Pfad vorliegt, die Medienelemente selbst jedoch nicht auf Gültigkeit überprüft werden, bevor Sie der Bibliothek hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="af24b-118">This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="af24b-119">Diese Methode akzeptiert sowohl statische als auch automatische Wiedergabelisten Dateien.</span><span class="sxs-lookup"><span data-stu-id="af24b-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="af24b-120">Die **iwmpplaylistcollection. importwiedergabe** -Methode kann auch verwendet werden, um der Bibliothek eine statische Wiedergabeliste hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="af24b-120">The **IWMPPlaylistCollection.importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="af24b-121">Vor dem Aufrufen dieser Methode müssen Sie über Vollzugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="af24b-121">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="af24b-122">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="af24b-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="af24b-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af24b-123">Examples</span></span>

<span data-ttu-id="af24b-124">Im folgenden Beispiel werden der Windows Media Player-Medien Auflistung drei Medienobjekte hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="af24b-124">The following example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="af24b-125">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="af24b-125">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a><span data-ttu-id="af24b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af24b-126">Requirements</span></span>



| <span data-ttu-id="af24b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af24b-127">Requirement</span></span> | <span data-ttu-id="af24b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="af24b-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af24b-129">Version</span><span class="sxs-lookup"><span data-stu-id="af24b-129">Version</span></span><br/>   | <span data-ttu-id="af24b-130">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="af24b-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="af24b-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="af24b-131">Namespace</span></span><br/> | <span data-ttu-id="af24b-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="af24b-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="af24b-133">Assembly</span><span class="sxs-lookup"><span data-stu-id="af24b-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="af24b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="af24b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af24b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af24b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af24b-136">**Iwmpmediacollection-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="af24b-136">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af24b-137">**Iwmpmediacollection. Remove (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="af24b-137">**IWMPMediaCollection.remove (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af24b-138">**Iwmpplaylistcollection. importwiedergabe (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="af24b-138">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





