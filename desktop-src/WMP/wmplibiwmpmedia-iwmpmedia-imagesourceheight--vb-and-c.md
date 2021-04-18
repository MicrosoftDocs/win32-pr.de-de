---
title: Iwmpmedia imagesourceheight (Eigenschaft)
description: Die imagesourceheight-Eigenschaft ruft die Höhe des aktuellen Medien Elements in Pixel ab.
ms.assetid: d60f1713-7110-4605-9009-45825c380546
keywords:
- imagesourceheight-Eigenschaften Fenster Media Player
- imagesourceheight-Eigenschaft, Windows Media Player, iwmpmedia-Schnittstelle
- Iwmpmedia Interface, Windows Media Player, imagesourceheight (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPMedia.imageSourceHeight
- IWMPMedia.get_imageSourceHeight
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b80a702f119ba72220e5ac3ac86b524ce8c11c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371518"
---
# <a name="iwmpmediaimagesourceheight-property"></a><span data-ttu-id="fffd4-106">Iwmpmedia:: imagesourceheight (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fffd4-106">IWMPMedia::imageSourceHeight property</span></span>

<span data-ttu-id="fffd4-107">Die **imagesourceheight** -Eigenschaft ruft die Höhe des aktuellen Medien Elements in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="fffd4-107">The **imageSourceHeight** property gets the height of the current media item in pixels.</span></span>

<span data-ttu-id="fffd4-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fffd4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffd4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fffd4-109">Syntax</span></span>


```CSharp
public System.Int32 imageSourceHeight {get;}
```


```VB

Public ReadOnly Property imageSourceHeight As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="fffd4-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fffd4-110">Property value</span></span>

<span data-ttu-id="fffd4-111">Ein **System. Int32** -Wert, der die Höhe des Medien Elements ist.</span><span class="sxs-lookup"><span data-stu-id="fffd4-111">A **System.Int32** that is the height of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="fffd4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fffd4-112">Remarks</span></span>

<span data-ttu-id="fffd4-113">Wenn das Medien Element nicht das aktuelle ist, gibt diese Eigenschaft 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="fffd4-113">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="fffd4-114">Vor der Verwendung dieser Eigenschaft müssen Sie über Lesezugriff auf die Bibliothek verfügen.</span><span class="sxs-lookup"><span data-stu-id="fffd4-114">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="fffd4-115">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fffd4-115">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fffd4-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fffd4-116">Examples</span></span>

<span data-ttu-id="fffd4-117">Im folgenden Beispiel wird **imagesourceheight** verwendet, um die Bildgröße des aktuellen Medien Elements in einem Textfeld in Pixel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fffd4-117">The following example uses **imageSourceHeight** to display the image size, in pixels, of the current media item in a text box.</span></span> <span data-ttu-id="fffd4-118">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="fffd4-118">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Store the height and width of the new media item.
         int height = player.currentMedia.imageSourceHeight;
         int width = player.currentMedia.imageSourceWidth;

         // Clear all the information in the text box.
         videoSize.Clear();

         // Test whether an image is visible.
         if (height != 0 && width != 0)
         {
            // Display the image size information.
            videoSize.Text = (width.ToString() + " x " + height.ToString());
         }
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = WMPLib.WMPOpenState.wmposMediaOpen) Then

        &#39; Store the height and width of the new media item.
        Dim Height As Integer = player.currentMedia.imageSourceHeight
        Dim Width As Integer = player.currentMedia.imageSourceWidth

        &#39; Clear all the information in the text box.
        videoSize.Clear()

        &#39; Test whether an image is visible.
        If (Height <> 0 And Width <> 0) Then

            &#39; Display the image size information.
            videoSize.Text = (Width.ToString() + &quot; x &quot; + Height.ToString())

        End If

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="fffd4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fffd4-119">Requirements</span></span>



| <span data-ttu-id="fffd4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fffd4-120">Requirement</span></span> | <span data-ttu-id="fffd4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fffd4-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffd4-122">Version</span><span class="sxs-lookup"><span data-stu-id="fffd4-122">Version</span></span><br/>   | <span data-ttu-id="fffd4-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="fffd4-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fffd4-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="fffd4-124">Namespace</span></span><br/> | <span data-ttu-id="fffd4-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fffd4-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fffd4-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="fffd4-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fffd4-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fffd4-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fffd4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fffd4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffd4-129">**Iwmpmedia-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fffd4-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





