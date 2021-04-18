---
title: Iwmpnetwork MaxBandwidth (Eigenschaft)
description: Mit der MaxBandwidth-Eigenschaft wird die maximal zulässige Bandbreite abgerufen oder festgelegt.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- MaxBandwidth-Eigenschaft, Windows Media Player
- MaxBandwidth-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, MaxBandwidth (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371628"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a><span data-ttu-id="ee567-106">Iwmpnetwork:: MaxBandwidth (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee567-106">IWMPNetwork::maxBandwidth property</span></span>

<span data-ttu-id="ee567-107">Mit der **MaxBandwidth** -Eigenschaft wird die maximal zulässige Bandbreite abgerufen oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee567-107">The **maxBandwidth** property gets or sets the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee567-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee567-108">Syntax</span></span>


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ee567-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ee567-109">Property value</span></span>

<span data-ttu-id="ee567-110">Ein **System. Int32** -Wert, der die maximale Bandbreite ist.</span><span class="sxs-lookup"><span data-stu-id="ee567-110">A **System.Int32** that is the maximum bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee567-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee567-111">Remarks</span></span>

<span data-ttu-id="ee567-112">Diese Eigenschaft hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="ee567-112">This property does not have a default value.</span></span> <span data-ttu-id="ee567-113">Der Wert kann bei der Wiedergabe von Windows Media Player angegeben werden, die Änderung wird jedoch erst wirksam, wenn das aktuelle Medien Element freigegeben wird, indem ein anderes geöffnet wird, oder durch Aufrufen von **AxWindowsMediaPlayer. Close**.</span><span class="sxs-lookup"><span data-stu-id="ee567-113">The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling **AxWindowsMediaPlayer.close**.</span></span> <span data-ttu-id="ee567-114">Windows Media Player versucht, eine möglichst hohe Bandbreite zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ee567-114">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="ee567-115">Es findet keine absichtliche Verringerung der Bandbreite statt, wenn dieser Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ee567-115">No intentional reduction of bandwidth will occur unless this value is set.</span></span>

<span data-ttu-id="ee567-116">Diese Einstellung ist nützlich, um die Menge der verwendeten Bandbreite zu reduzieren, insbesondere im Fall eines MBR-Streams (Multiple Bitrate).</span><span class="sxs-lookup"><span data-stu-id="ee567-116">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="ee567-117">Ein MBR-Datenstrom enthält mehrere Datenströme mit unterschiedlichen Bitraten.</span><span class="sxs-lookup"><span data-stu-id="ee567-117">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="ee567-118">In einigen Fällen kann es wünschenswert sein, einen Datenstrom mit einer niedrigeren Bitrate zu verwenden, als dies für den Client erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ee567-118">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="ee567-119">Wenn Sie in diesem Fall eine niedrigere Bitrate mit der **iwmpnetwork. MaxBandwidth** -Eigenschaft angeben, wird ein niedrigerer Bitrate-Stream ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="ee567-119">In this case, specifying a lower bit rate with the **IWMPNetwork.maxBandwidth** property will select a lower bit-rate stream.</span></span> <span data-ttu-id="ee567-120">Ein MBR-Datenstrom kann beispielsweise Datenströme enthalten, die mit 20 kbit pro Sekunde (Kbit/s), 37 Kbit/s und 200 Kbit/s codiert</span><span class="sxs-lookup"><span data-stu-id="ee567-120">For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="ee567-121">Wenn Sie mithilfe von **iwmpnetwork. MaxBandwidth** eine Bitrate von 50.000 (50 KBit/s) angeben, wird der Datenstrom 37 Kbit/s anstelle des Datenstroms von 200 Kbit/s ausgewählt</span><span class="sxs-lookup"><span data-stu-id="ee567-121">Using **IWMPNetwork.maxBandwidth** to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee567-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee567-122">Requirements</span></span>



| <span data-ttu-id="ee567-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee567-123">Requirement</span></span> | <span data-ttu-id="ee567-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ee567-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee567-125">Version</span><span class="sxs-lookup"><span data-stu-id="ee567-125">Version</span></span><br/>   | <span data-ttu-id="ee567-126">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ee567-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ee567-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee567-127">Namespace</span></span><br/> | <span data-ttu-id="ee567-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ee567-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ee567-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="ee567-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ee567-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ee567-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee567-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee567-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee567-132">**AxWindowsMediaPlayer. Close (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee567-132">**AxWindowsMediaPlayer.close (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="ee567-133">**Iwmpnetwork-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee567-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





