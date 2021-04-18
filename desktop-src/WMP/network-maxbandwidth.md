---
title: Network. MaxBandwidth
description: Die MaxBandwidth-Eigenschaft gibt die maximal zulässige Bandbreite an oder ruft Sie ab.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Windows Media Player "Network. MaxBandwidth"
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365171"
---
# <a name="networkmaxbandwidth"></a><span data-ttu-id="9ebba-104">Network. MaxBandwidth</span><span class="sxs-lookup"><span data-stu-id="9ebba-104">Network.maxBandwidth</span></span>

<span data-ttu-id="9ebba-105">Die **MaxBandwidth** -Eigenschaft gibt die maximal zulässige Bandbreite an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="9ebba-105">The **maxBandwidth** property specifies or retrieves the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ebba-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ebba-106">Syntax</span></span>

<span data-ttu-id="9ebba-107">*Player*. *Netzwerk*. **MaxBandwidth**</span><span class="sxs-lookup"><span data-stu-id="9ebba-107">*player*.*network*.**maxBandwidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9ebba-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="9ebba-108">Possible Values</span></span>

<span data-ttu-id="9ebba-109">Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**). </span><span class="sxs-lookup"><span data-stu-id="9ebba-109">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="9ebba-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ebba-110">Remarks</span></span>

<span data-ttu-id="9ebba-111">Diese Eigenschaft hat keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9ebba-111">This property has no default value.</span></span> <span data-ttu-id="9ebba-112">Der Wert kann bei der Wiedergabe von Windows-Media Player angegeben werden, die Änderung wird jedoch erst wirksam, wenn das aktuelle Medien Element durch Öffnen eines weiteren oder durch Aufrufen von *Player* freigegeben wird. **Schließen** Sie.</span><span class="sxs-lookup"><span data-stu-id="9ebba-112">Its value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling *Player*.**close**.</span></span> <span data-ttu-id="9ebba-113">Windows Media Player versucht, eine möglichst hohe Bandbreite zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="9ebba-113">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="9ebba-114">Nur wenn der Wert festgelegt wird, wird die Bandbreiten Reduzierung durchgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9ebba-114">Only in the case of the value being set will any bandwidth reduction occur.</span></span>

<span data-ttu-id="9ebba-115">Diese Einstellung ist nützlich, um die Menge der verwendeten Bandbreite zu reduzieren, insbesondere im Fall eines MBR-Streams (Multiple Bitrate).</span><span class="sxs-lookup"><span data-stu-id="9ebba-115">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="9ebba-116">Ein MBR-Datenstrom enthält mehrere Datenströme mit unterschiedlichen Bitraten.</span><span class="sxs-lookup"><span data-stu-id="9ebba-116">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="9ebba-117">In einigen Fällen kann es wünschenswert sein, einen Datenstrom mit einer niedrigeren Bitrate zu verwenden, als dies für den Client erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9ebba-117">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="9ebba-118">Wenn Sie in diesem Fall die **MaxBandwidth** -Eigenschaft festlegen, wird ein niedrigerer Bitrate-Stream ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9ebba-118">In this case, setting the **maxBandwidth** property will select a lower bit-rate stream.</span></span>

<span data-ttu-id="9ebba-119">Ein MBR-Datenstrom könnte beispielsweise Datenströme enthalten, die mit 20 kbit pro Sekunde (Kbit/s), 37 Kbit/s und 200 Kbit/s codiert</span><span class="sxs-lookup"><span data-stu-id="9ebba-119">For example, an MBR stream could include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="9ebba-120">Wenn Sie die **MaxBandwidth** -Eigenschaft auf 50.000 (50 KBit/s) festlegen, wird der Datenstrom 37 Kbit/s anstelle des Datenstroms der Größe 200 (</span><span class="sxs-lookup"><span data-stu-id="9ebba-120">Setting the **maxBandwidth** property to 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ebba-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ebba-121">Requirements</span></span>



| <span data-ttu-id="9ebba-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ebba-122">Requirement</span></span> | <span data-ttu-id="9ebba-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9ebba-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9ebba-124">Version</span><span class="sxs-lookup"><span data-stu-id="9ebba-124">Version</span></span><br/> | <span data-ttu-id="9ebba-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="9ebba-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9ebba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9ebba-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ebba-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ebba-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ebba-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ebba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ebba-129">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="9ebba-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="9ebba-130">**Player. Close**</span><span class="sxs-lookup"><span data-stu-id="9ebba-130">**Player.close**</span></span>](player-close.md)
</dt> </dl>

 

 





