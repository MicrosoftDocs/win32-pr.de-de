---
title: AxWindowsMediaPlayer. openstate (Eigenschaft)
description: Die openstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand der Inhaltsquelle angibt.
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- openstate-Eigenschaften Fenster Media Player
- openstate-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, openstate (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357990"
---
# <a name="axwindowsmediaplayeropenstate-property"></a><span data-ttu-id="3fe37-106">AxWindowsMediaPlayer. openstate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3fe37-106">AxWindowsMediaPlayer.openState property</span></span>

<span data-ttu-id="3fe37-107">Die openstate-Eigenschaft ruft einen Enumerationswert ab, der den Zustand der Inhaltsquelle angibt.</span><span class="sxs-lookup"><span data-stu-id="3fe37-107">The openState property gets an enumeration value indicating the state of the content source.</span></span>

<span data-ttu-id="3fe37-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="3fe37-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe37-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fe37-109">Syntax</span></span>


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a><span data-ttu-id="3fe37-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="3fe37-110">Property value</span></span>

<span data-ttu-id="3fe37-111">Der WMPLib. wmpopenstate-Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="3fe37-111">The WMPLib.WMPOpenState enumeration value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fe37-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fe37-112">Remarks</span></span>

<span data-ttu-id="3fe37-113">Es ist nicht garantiert, dass Windows-Media Player Zustände in einer bestimmten Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="3fe37-113">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="3fe37-114">Außerdem treten nicht alle Zustände notwendigerweise während einer Sequenz von Ereignissen auf.</span><span class="sxs-lookup"><span data-stu-id="3fe37-114">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="3fe37-115">Sie sollten keinen Code schreiben, der auf der Status Reihenfolge basiert.</span><span class="sxs-lookup"><span data-stu-id="3fe37-115">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fe37-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fe37-116">Requirements</span></span>



| <span data-ttu-id="3fe37-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fe37-117">Requirement</span></span> | <span data-ttu-id="3fe37-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3fe37-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe37-119">Version</span><span class="sxs-lookup"><span data-stu-id="3fe37-119">Version</span></span><br/>   | <span data-ttu-id="3fe37-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="3fe37-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3fe37-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="3fe37-121">Namespace</span></span><br/> | <span data-ttu-id="3fe37-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="3fe37-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3fe37-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="3fe37-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3fe37-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3fe37-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fe37-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fe37-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fe37-126">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="3fe37-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3fe37-127">**AxWindowsMediaPlayer. OpenStateChange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="3fe37-127">**AxWindowsMediaPlayer.OpenStateChange Event**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="3fe37-128">**WMPLib. wmpopenstate**</span><span class="sxs-lookup"><span data-stu-id="3fe37-128">**WMPLib.WMPOpenState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





