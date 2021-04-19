---
title: AxWindowsMediaPlayer. URL (Eigenschaft)
description: Die URL-Eigenschaft ruft den Namen des wieder zugebende Medien Elements ab oder legt ihn fest.
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- URL-Eigenschaften Fenster Media Player
- URL-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, URL-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ed9e601aa581e988bac1a233f06c4f5c552353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356007"
---
# <a name="axwindowsmediaplayerurl-property"></a><span data-ttu-id="f3a92-106">AxWindowsMediaPlayer. URL (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3a92-106">AxWindowsMediaPlayer.URL property</span></span>

<span data-ttu-id="f3a92-107">Die URL-Eigenschaft ruft den Namen des wieder zugebende Medien Elements ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="f3a92-107">The URL property gets or sets the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a92-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3a92-108">Syntax</span></span>


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a><span data-ttu-id="f3a92-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f3a92-109">Property value</span></span>

<span data-ttu-id="f3a92-110">Ein System. String-Wert, der die URL des Medien Elements ist.</span><span class="sxs-lookup"><span data-stu-id="f3a92-110">A System.String that is the URL of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a92-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3a92-111">Remarks</span></span>

<span data-ttu-id="f3a92-112">Diese Eigenschaft kann nur auf eine URL in einer Sicherheitszone festgelegt werden, die identisch ist oder weniger restriktiv ist als die Sicherheitszone des aufrufenden Programms oder der Webseite.</span><span class="sxs-lookup"><span data-stu-id="f3a92-112">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="f3a92-113">Anwendungen, die Medienelemente hinter einer Firewall öffnen, haben eine bessere Leistung, wenn die Adresse anstelle der IP-Adresse mit dem DNS-Namen (Domain Nameserver) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3a92-113">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="f3a92-114">Diese Methode kann nicht aus dem Ereignishandlercode aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f3a92-114">Do not call this method from event handler code.</span></span> <span data-ttu-id="f3a92-115">Das Aufrufen von **URL** von einem Ereignishandler kann zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="f3a92-115">Calling **URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="f3a92-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3a92-116">Examples</span></span>

<span data-ttu-id="f3a92-117">Im folgenden Beispiel kann der Benutzer eine Mediendatei angeben, indem er einen Dateipfad in ein Textfeld eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f3a92-117">The following example allows the user to specify a media file by entering a file path in a text box.</span></span> <span data-ttu-id="f3a92-118">Wenn auf eine Schaltfläche geklickt wird, wird die URL-Eigenschaft auf die angegebene Datei festgelegt, und die Datei wird wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="f3a92-118">When a button is clicked, the URL property is set to the specified file and the file is played.</span></span> <span data-ttu-id="f3a92-119">Das AxWMPLib. AxWindowsMediaPlayer-Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f3a92-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f3a92-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3a92-120">Requirements</span></span>



| <span data-ttu-id="f3a92-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3a92-121">Requirement</span></span> | <span data-ttu-id="f3a92-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f3a92-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a92-123">Version</span><span class="sxs-lookup"><span data-stu-id="f3a92-123">Version</span></span><br/>   | <span data-ttu-id="f3a92-124">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="f3a92-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f3a92-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3a92-125">Namespace</span></span><br/> | <span data-ttu-id="f3a92-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="f3a92-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f3a92-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="f3a92-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f3a92-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f3a92-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a92-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3a92-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a92-130">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="f3a92-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





