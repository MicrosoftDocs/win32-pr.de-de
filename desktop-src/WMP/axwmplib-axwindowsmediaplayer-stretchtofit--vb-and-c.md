---
title: AxWindowsMediaPlayer. stretchdefit (Eigenschaft)
description: Mit der Eigenschaft stretchdefit wird ein Wert abgerufen oder festgelegt, der angibt, ob die Größe des Videos, das vom Windows Media Player-Steuerelement angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Eigenschaften Fenster für stretchdefit-Eigenschaft Media Player
- stretchdefit-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, stretchdefit (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354675"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a><span data-ttu-id="d5acc-106">AxWindowsMediaPlayer. stretchdefit (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d5acc-106">AxWindowsMediaPlayer.stretchToFit property</span></span>

<span data-ttu-id="d5acc-107">Mit der Eigenschaft stretchdefit wird ein Wert abgerufen oder festgelegt, der angibt, ob die Größe des Videos, das vom Windows Media Player-Steuerelement angezeigt wird, automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Video Bilds</span><span class="sxs-lookup"><span data-stu-id="d5acc-107">The stretchToFit property gets or sets a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5acc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5acc-108">Syntax</span></span>


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="d5acc-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d5acc-109">Property value</span></span>

<span data-ttu-id="d5acc-110">Der System. Boolean-Wert, der angibt, ob das Video so gestreckt wird, dass es an das Fenster angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="d5acc-110">The System.Boolean value that indicates whether the video will stretch to fit the window.</span></span> <span data-ttu-id="d5acc-111">Der Standardwert ist „FALSE“.</span><span class="sxs-lookup"><span data-stu-id="d5acc-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5acc-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5acc-112">Remarks</span></span>

<span data-ttu-id="d5acc-113">Wenn **stretchdefit** auf true festgelegt ist, wird das ursprüngliche Seitenverhältnis des Videos vom Windows Media Player-Steuerelement beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d5acc-113">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="d5acc-114">Wenn das Seitenverhältnis des Videos nicht mit dem Seitenverhältnis des Videofensters identisch ist, können schwarze Masken Bereiche entweder am oberen und unteren Rand des Video Bilds angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d5acc-114">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="d5acc-115">Diese Eigenschaft gilt nur für das Windows Media Player-Steuerelement, wenn es in eine Webseite eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="d5acc-115">This property applies to the Windows Media Player control only when it is embedded in a webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5acc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5acc-116">Requirements</span></span>



| <span data-ttu-id="d5acc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5acc-117">Requirement</span></span> | <span data-ttu-id="d5acc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d5acc-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5acc-119">Version</span><span class="sxs-lookup"><span data-stu-id="d5acc-119">Version</span></span><br/>   | <span data-ttu-id="d5acc-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="d5acc-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d5acc-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5acc-121">Namespace</span></span><br/> | <span data-ttu-id="d5acc-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d5acc-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d5acc-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="d5acc-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d5acc-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d5acc-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5acc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5acc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5acc-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="d5acc-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





