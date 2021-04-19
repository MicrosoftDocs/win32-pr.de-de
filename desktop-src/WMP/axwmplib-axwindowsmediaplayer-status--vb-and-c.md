---
title: AxWindowsMediaPlayer. Status (Eigenschaft)
description: Die Status-Eigenschaft ruft einen Wert ab, der den Status von Windows Media Player angibt.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Status Eigenschaften Fenster Media Player
- Status-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, Status-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372062"
---
# <a name="axwindowsmediaplayerstatus-property"></a><span data-ttu-id="2d579-106">AxWindowsMediaPlayer. Status (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2d579-106">AxWindowsMediaPlayer.status property</span></span>

<span data-ttu-id="2d579-107">Die Status-Eigenschaft ruft einen Wert ab, der den Status von Windows Media Player angibt.</span><span class="sxs-lookup"><span data-stu-id="2d579-107">The status property gets a value indicating the status of Windows Media Player.</span></span>

<span data-ttu-id="2d579-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2d579-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d579-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d579-109">Syntax</span></span>


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a><span data-ttu-id="2d579-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2d579-110">Property value</span></span>

<span data-ttu-id="2d579-111">Die System. String-Wert, der den Status hat.</span><span class="sxs-lookup"><span data-stu-id="2d579-111">The System.String that is the status.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d579-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d579-112">Remarks</span></span>

<span data-ttu-id="2d579-113">Die in dieser Eigenschaft enthaltenen Werte können jederzeit geändert werden und sollten nur zu Anzeige Zwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d579-113">The values contained in this property are subject to change at any time, and should be used for display purposes only.</span></span>

<span data-ttu-id="2d579-114">Der AxWindowsMediaPlayer. Das **statusChange** -Ereignis wird ausgelöst, wenn der Wert dieser Eigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2d579-114">The AxWindowsMediaPlayer.**StatusChange** event is fired whenever this property changes value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d579-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d579-115">Requirements</span></span>



| <span data-ttu-id="2d579-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d579-116">Requirement</span></span> | <span data-ttu-id="2d579-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2d579-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d579-118">Version</span><span class="sxs-lookup"><span data-stu-id="2d579-118">Version</span></span><br/>   | <span data-ttu-id="2d579-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2d579-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="2d579-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d579-120">Namespace</span></span><br/> | <span data-ttu-id="2d579-121">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="2d579-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="2d579-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="2d579-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2d579-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2d579-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d579-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d579-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d579-125">**AxWindowsMediaPlayer-Objekt (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2d579-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2d579-126">**AxWindowsMediaPlayer. statusChange-Ereignis (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2d579-126">**AxWindowsMediaPlayer.StatusChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





