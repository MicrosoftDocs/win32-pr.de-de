---
title: AxWindowsMediaPlayer. windowlessvideo (Eigenschaft)
description: Mit der windowlessvideo-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- windowlessvideo-Eigenschaften Fenster Media Player
- windowlessvideo-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, windowlessvideo (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367218"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a><span data-ttu-id="4c018-106">AxWindowsMediaPlayer. windowlessvideo (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="4c018-106">AxWindowsMediaPlayer.windowlessVideo property</span></span>

<span data-ttu-id="4c018-107">Mit der windowlessvideo-Eigenschaft wird ein Wert abgerufen oder festgelegt, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.</span><span class="sxs-lookup"><span data-stu-id="4c018-107">The windowlessVideo property gets or sets a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c018-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c018-108">Syntax</span></span>


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="4c018-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4c018-109">Property value</span></span>

<span data-ttu-id="4c018-110">Ein System. Boolean-Wert, der angibt, ob das Windows Media Player-Steuerelement Videos im fensterlosen Modus rendert.</span><span class="sxs-lookup"><span data-stu-id="4c018-110">A System.Boolean value indicating whether the Windows Media Player control renders video in windowless mode.</span></span> <span data-ttu-id="4c018-111">Der Standardwert ist „FALSE“.</span><span class="sxs-lookup"><span data-stu-id="4c018-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c018-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c018-112">Remarks</span></span>

<span data-ttu-id="4c018-113">Standardmäßig rendert ein eingebettetes Windows-Media Player-Steuerelement Videos in einem eigenen Fenster innerhalb des Client Bereichs.</span><span class="sxs-lookup"><span data-stu-id="4c018-113">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="4c018-114">Wenn **windowlessvideo** auf "true" festgelegt ist, rendert das Windows-Media Player-Objekt Video direkt im Client Bereich, sodass Sie besondere Effekte anwenden oder das Video mit Text auf eine Ebene anwenden können.</span><span class="sxs-lookup"><span data-stu-id="4c018-114">When **windowlessVideo** is set to true, the Windows Media Player object renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="4c018-115">In Windows Vista kann das Rendern von Videos im fensterlosen Modus die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="4c018-115">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="4c018-116">Das erhalten eines Werts für diese Eigenschaft wird für den Netscape-Navigator nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c018-116">Getting a value for this property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="4c018-117">Wenn Sie einen Wert für diese Eigenschaft in Netscape Navigator festlegen, kann dies zu unerwarteten Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="4c018-117">Setting a value for this property in Netscape Navigator may yield unexpected results.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c018-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c018-118">Requirements</span></span>



| <span data-ttu-id="4c018-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c018-119">Requirement</span></span> | <span data-ttu-id="4c018-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4c018-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c018-121">Version</span><span class="sxs-lookup"><span data-stu-id="4c018-121">Version</span></span><br/>   | <span data-ttu-id="4c018-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="4c018-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="4c018-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="4c018-123">Namespace</span></span><br/> | <span data-ttu-id="4c018-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="4c018-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="4c018-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="4c018-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c018-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4c018-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c018-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c018-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c018-128">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="4c018-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





