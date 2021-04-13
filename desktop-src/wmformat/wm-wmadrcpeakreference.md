---
title: WM/wmadrcpeer Reference
description: Das WM/wmadrcpeakreference-Attribut enthält die maximale Volumeebene der Datei als codiert. Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet. Dieser Wert wird vom Codec festgelegt und ist schreibgeschützt.
ms.assetid: c732ee88-437b-4970-8f17-61aed2d91022
keywords:
- WM/wmadrcpeer Reference Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMADRCPeakReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59660f950c748c45a1affccee10ae86e38998f23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389215"
---
# <a name="wmwmadrcpeakreference"></a><span data-ttu-id="0b61e-106">WM/wmadrcpeer Reference</span><span class="sxs-lookup"><span data-stu-id="0b61e-106">WM/WMADRCPeakReference</span></span>

<span data-ttu-id="0b61e-107">Das **WM/wmadrcpeakreference-** Attribut enthält die maximale Volumeebene der Datei als codiert.</span><span class="sxs-lookup"><span data-stu-id="0b61e-107">The **WM/WMADRCPeakReference** attribute contains the maximum volume level of the file as encoded.</span></span> <span data-ttu-id="0b61e-108">Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0b61e-108">This value is used by Windows Media Player for dynamic range control.</span></span> <span data-ttu-id="0b61e-109">Dieser Wert wird vom Codec festgelegt und ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0b61e-109">This value is set by the codec and is read-only.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0b61e-110">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="0b61e-110">Global Constant</span></span>

<span data-ttu-id="0b61e-111">g \_ wszwmwmadrcpeer Reference</span><span class="sxs-lookup"><span data-stu-id="0b61e-111">g\_wszWMWMADRCPeakReference</span></span>

## <a name="data-type"></a><span data-ttu-id="0b61e-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0b61e-112">Data Type</span></span>

<span data-ttu-id="0b61e-113">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0b61e-113">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0b61e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b61e-114">Remarks</span></span>

<span data-ttu-id="0b61e-115">Es gibt vier Attribute, die von Windows-Media Player für das dynamische Bereichs Steuerelement verwendet werden: **WM/wmadrcaveragereferenzierung**, **WM/wmadrcpeer Reference**, **WM/wmadrcaveragetarget** und **WM/wmadrcpeer Target**.</span><span class="sxs-lookup"><span data-stu-id="0b61e-115">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="0b61e-116">Alle diese Werte werden vom Writer auf der Grundlage von Informationen aus dem Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional-Codec geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0b61e-116">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="0b61e-117">Die durchschnittlichen Werte werden auf die durchschnittliche Volumeebene des Streams festgelegt, und die Spitzenwerte werden auf die maximale Volumeebene im Stream festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b61e-117">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="0b61e-118">Die Verweis Werte sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0b61e-118">The reference values are read-only.</span></span> <span data-ttu-id="0b61e-119">Die Zielwerte werden von Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen für die dynamische Bereichs Kontrolle des Benutzers aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="0b61e-119">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b61e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b61e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b61e-121">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="0b61e-121">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="0b61e-122">**WM/wmadrcaveragereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="0b61e-122">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="0b61e-123">**WM/wmadrcaveragetarget**</span><span class="sxs-lookup"><span data-stu-id="0b61e-123">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="0b61e-124">**WM/wmadrcpeer Target**</span><span class="sxs-lookup"><span data-stu-id="0b61e-124">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




