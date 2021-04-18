---
title: Iwmpsettings-Balance (Eigenschaft)
description: Die Balance-Eigenschaft ruft den aktuellen Stereo Saldo ab oder legt ihn fest.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- Ausgleichen der Eigenschaften Fenster Media Player
- Balance-Eigenschaften Fenster Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows-Media Player, Balance-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354680"
---
# <a name="iwmpsettingsbalance-property"></a><span data-ttu-id="31591-106">Iwmpsettings:: Balance (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="31591-106">IWMPSettings::balance property</span></span>

<span data-ttu-id="31591-107">Die **Balance** -Eigenschaft ruft den aktuellen Stereo Saldo ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="31591-107">The **balance** property gets or sets the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="31591-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="31591-108">Syntax</span></span>


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="31591-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="31591-109">Property value</span></span>

<span data-ttu-id="31591-110">Ein **System. Int32** -Wert, der den Saldo-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="31591-110">A **System.Int32** that is the balance value.</span></span> <span data-ttu-id="31591-111">Dieser Wert kann zwischen 100 und 100 liegen.</span><span class="sxs-lookup"><span data-stu-id="31591-111">This value can range from  100 to 100.</span></span> <span data-ttu-id="31591-112">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="31591-112">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="31591-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31591-113">Remarks</span></span>

<span data-ttu-id="31591-114">Der Wert 0 (null) gibt an, dass die Audiodaten gleichzeitig auf dem linken und rechten Kanal abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="31591-114">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="31591-115">Der Wert 100 gibt an, dass Audioinhalte nur im linken Kanal abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="31591-115">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="31591-116">Der Wert 100 gibt an, dass Audioinhalte nur auf dem rechten Kanal abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="31591-116">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="31591-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31591-117">Requirements</span></span>



| <span data-ttu-id="31591-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31591-118">Requirement</span></span> | <span data-ttu-id="31591-119">Wert</span><span class="sxs-lookup"><span data-stu-id="31591-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31591-120">Version</span><span class="sxs-lookup"><span data-stu-id="31591-120">Version</span></span><br/>   | <span data-ttu-id="31591-121">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="31591-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="31591-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="31591-122">Namespace</span></span><br/> | <span data-ttu-id="31591-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="31591-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="31591-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="31591-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="31591-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="31591-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31591-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31591-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31591-127">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="31591-127">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





