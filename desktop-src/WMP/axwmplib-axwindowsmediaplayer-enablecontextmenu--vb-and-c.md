---
title: AxWindowsMediaPlayer. enablecontextmenu (Eigenschaft)
description: Die enablecontextmenu-Eigenschaft ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das beim Klicken mit der rechten Maustaste angezeigt wird, oder legt diesen fest.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- enablecontextmenu-Eigenschaft, Windows-Media Player
- enablecontextmenu-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, enablecontextmenu (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365174"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a><span data-ttu-id="17b39-106">AxWindowsMediaPlayer. enablecontextmenu (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="17b39-106">AxWindowsMediaPlayer.enableContextMenu property</span></span>

<span data-ttu-id="17b39-107">Die enablecontextmenu-Eigenschaft ruft einen Wert ab, der angibt, ob das Kontextmenü aktiviert werden soll, das beim Klicken mit der rechten Maustaste angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="17b39-107">The enableContextMenu property gets or sets a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b39-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="17b39-108">Syntax</span></span>


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="17b39-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="17b39-109">Property value</span></span>

<span data-ttu-id="17b39-110">Ein System. Boolean-Wert, der angibt, ob das Kontextmenü aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b39-110">A System.Boolean value that indicates whether to enable the context menu.</span></span> <span data-ttu-id="17b39-111">Der Standardwert lautet „true“.</span><span class="sxs-lookup"><span data-stu-id="17b39-111">The default value is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="17b39-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17b39-112">Remarks</span></span>

<span data-ttu-id="17b39-113">Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.</span><span class="sxs-lookup"><span data-stu-id="17b39-113">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="requirements"></a><span data-ttu-id="17b39-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17b39-114">Requirements</span></span>



| <span data-ttu-id="17b39-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17b39-115">Requirement</span></span> | <span data-ttu-id="17b39-116">Wert</span><span class="sxs-lookup"><span data-stu-id="17b39-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b39-117">Version</span><span class="sxs-lookup"><span data-stu-id="17b39-117">Version</span></span><br/>   | <span data-ttu-id="17b39-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="17b39-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="17b39-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="17b39-119">Namespace</span></span><br/> | <span data-ttu-id="17b39-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="17b39-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="17b39-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="17b39-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="17b39-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="17b39-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b39-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17b39-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b39-124">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="17b39-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





