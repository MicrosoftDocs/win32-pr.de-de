---
title: AxWindowsMediaPlayer. currentMedia (Eigenschaft)
description: Die currentMedia-Eigenschaft ruft die iwmpmedia-Schnittstelle ab, die dem aktuellen Medien Element entspricht, oder legt diese fest.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- currentMedia-Eigenschaften Fenster Media Player
- currentMedia-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, currentMedia-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354723"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a><span data-ttu-id="618c3-106">AxWindowsMediaPlayer. currentMedia (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="618c3-106">AxWindowsMediaPlayer.currentMedia property</span></span>

<span data-ttu-id="618c3-107">Die currentMedia-Eigenschaft ruft die iwmpmedia-Schnittstelle ab, die dem aktuellen Medien Element entspricht, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="618c3-107">The currentMedia property gets or sets the IWMPMedia interface that corresponds to the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="618c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="618c3-108">Syntax</span></span>


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="618c3-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="618c3-109">Property value</span></span>

<span data-ttu-id="618c3-110">Die WMPLib. iwmpmedia-Schnittstelle, die Zugriff auf das aktuelle Medien Element bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="618c3-110">The WMPLib.IWMPMedia interface that provides access to the current media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="618c3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="618c3-111">Remarks</span></span>

<span data-ttu-id="618c3-112">Wenn AxWindowsMediaPlayer. Settings. die **Autostart** -Eigenschaft ist "true". die Wiedergabe beginnt automatisch, wenn Sie **currentMedia** festlegen.</span><span class="sxs-lookup"><span data-stu-id="618c3-112">If the AxWindowsMediaPlayer.settings.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="618c3-113">Sie können eine iwmpmedia-Schnittstelle für ein bestimmtes Medien Element über die iwmpwiedergabe. Item-Eigenschaft (die iwmpwiedergabe. get \_ Item-Methode in c#) abrufen.</span><span class="sxs-lookup"><span data-stu-id="618c3-113">You can retrieve an IWMPMedia interface for a given media item through the IWMPPlaylist.Item property (the IWMPPlaylist.get\_Item method in C#).</span></span> <span data-ttu-id="618c3-114">Wenn Sie ein Medien Element mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest, oder verwenden Sie newmedia.</span><span class="sxs-lookup"><span data-stu-id="618c3-114">To load a media item using a file name, set the URL property or use newMedia.</span></span>

## <a name="examples"></a><span data-ttu-id="618c3-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="618c3-115">Examples</span></span>

<span data-ttu-id="618c3-116">Im folgenden Beispiel wird das erste Medien Element in der Bibliothek abgerufen und die currentMedia-Eigenschaft verwendet, um das abgerufene Medien Element als Aktuelles Medien Element festzulegen und seinen Namen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="618c3-116">The following example retrieves the first media item in the library and uses the currentMedia property to set the retrieved media item as the current media item and display its name.</span></span> <span data-ttu-id="618c3-117">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="618c3-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a><span data-ttu-id="618c3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="618c3-118">Requirements</span></span>



| <span data-ttu-id="618c3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="618c3-119">Requirement</span></span> | <span data-ttu-id="618c3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="618c3-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="618c3-121">Version</span><span class="sxs-lookup"><span data-stu-id="618c3-121">Version</span></span><br/>   | <span data-ttu-id="618c3-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="618c3-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="618c3-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="618c3-123">Namespace</span></span><br/> | <span data-ttu-id="618c3-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="618c3-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="618c3-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="618c3-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="618c3-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="618c3-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="618c3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="618c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="618c3-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="618c3-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="618c3-129">**AxWindowsMediaPlayer. newmedia (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="618c3-129">**AxWindowsMediaPlayer.newMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[<span data-ttu-id="618c3-130">**AxWindowsMediaPlayer. URL (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="618c3-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="618c3-131">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="618c3-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="618c3-132">**Iwmpwiedergabe. Item (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="618c3-132">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="618c3-133">**Iwmpsettings. Autostart (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="618c3-133">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





