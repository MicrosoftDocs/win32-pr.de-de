---
title: KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts
description: Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird. | KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Das KeyPress-Ereignis der AxWindowsMediaPlayer-Objekt Fenster Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352082"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d09dc-105">KeyPress-Ereignis des AxWindowsMediaPlayer-Objekts</span><span class="sxs-lookup"><span data-stu-id="d09dc-105">KeyPress Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d09dc-106">Das KeyPress-Ereignis tritt auf, wenn eine Taste gedrückt und freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d09dc-106">The KeyPress event occurs when a key is pressed and released.</span></span>

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a><span data-ttu-id="d09dc-107">Ereignisdaten</span><span class="sxs-lookup"><span data-stu-id="d09dc-107">Event Data</span></span>

<span data-ttu-id="d09dc-108">Der diesem Ereignis zugeordnete Handler ist vom Typ **AxWMPLib. \_ Wmpocxevents \_ KeyPressEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="d09dc-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEventHandler**.</span></span> <span data-ttu-id="d09dc-109">Dieser Handler empfängt ein Argument vom Typ **AxWMPLib. \_ Wmpocxevents \_ KeyPressEvent**, das die folgende Eigenschaft enthält, die sich auf dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="d09dc-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyPressEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d09dc-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d09dc-110">Property</span></span>      | <span data-ttu-id="d09dc-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d09dc-111">Description</span></span>                                                                        |
|---------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d09dc-112">**nkeyascii**</span><span class="sxs-lookup"><span data-stu-id="d09dc-112">**nKeyAscii**</span></span> | <span data-ttu-id="d09dc-113">System. Int16Specifies der numerische Standard-ANSI-Code für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="d09dc-113">System.Int16Specifies the standard numeric ANSI code for the character.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d09dc-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d09dc-114">Remarks</span></span>

<span data-ttu-id="d09dc-115">Dieses Ereignis tritt auf, wenn die Tastatureingabe ein beliebiges druckbares Tastatur Zeichen ergibt, die STRG-Taste mit einem Zeichen aus dem Standard Alphabet oder einem von einigen Sonderzeichen und der Eingabe-oder RÜCKTASTE gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d09dc-115">This event occurs when the keystroke results in any printable keyboard character, the CTRL key combined with a character from the standard alphabet or one of a few special characters, and the ENTER or BACKSPACE key.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09dc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d09dc-116">Requirements</span></span>



| <span data-ttu-id="d09dc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d09dc-117">Requirement</span></span> | <span data-ttu-id="d09dc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d09dc-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d09dc-119">Version</span><span class="sxs-lookup"><span data-stu-id="d09dc-119">Version</span></span><br/>   | <span data-ttu-id="d09dc-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="d09dc-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d09dc-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d09dc-121">Namespace</span></span><br/> | <span data-ttu-id="d09dc-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d09dc-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d09dc-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="d09dc-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d09dc-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d09dc-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09dc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d09dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09dc-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d09dc-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





