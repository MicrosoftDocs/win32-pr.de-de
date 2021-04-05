---
title: WM/wmadrcpeer Target
description: Das WM/wmadrcpeaktarget-Attribut enthält die maximale Volumeebene, die vom Benutzer angefordert wurde. Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet.
ms.assetid: 94ef5db1-34f4-4cf8-ac56-c85cca10536b
keywords:
- WM/wmadrcpeer Target Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMADRCPeakTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55eac4ea68cd61e2cfa0b5c185dc1a4ad17e5ce8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718611"
---
# <a name="wmwmadrcpeaktarget"></a><span data-ttu-id="bac61-105">WM/wmadrcpeer Target</span><span class="sxs-lookup"><span data-stu-id="bac61-105">WM/WMADRCPeakTarget</span></span>

<span data-ttu-id="bac61-106">Das **WM/wmadrcpeaktarget-** Attribut enthält die maximale Volumeebene, die vom Benutzer angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="bac61-106">The **WM/WMADRCPeakTarget** attribute contains the maximum volume level requested by the user.</span></span> <span data-ttu-id="bac61-107">Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bac61-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="bac61-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="bac61-108">Global Constant</span></span>

<span data-ttu-id="bac61-109">g \_ wszwmwmadrcpeer-Ziel</span><span class="sxs-lookup"><span data-stu-id="bac61-109">g\_wszWMWMADRCPeakTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="bac61-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bac61-110">Data Type</span></span>

<span data-ttu-id="bac61-111">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bac61-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="bac61-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bac61-112">Remarks</span></span>

<span data-ttu-id="bac61-113">Es gibt vier Attribute, die von Windows-Media Player für das dynamische Bereichs Steuerelement verwendet werden: **WM/wmadrcaveragereferenzierung**, **WM/wmadrcpeer Reference**, **WM/wmadrcaveragetarget** und **WM/wmadrcpeer Target**.</span><span class="sxs-lookup"><span data-stu-id="bac61-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="bac61-114">Alle diese Werte werden vom Writer auf der Grundlage von Informationen aus dem Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional-Codec geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bac61-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="bac61-115">Die durchschnittlichen Werte werden auf die durchschnittliche Volumeebene des Streams festgelegt, und die Spitzenwerte werden auf die maximale Volumeebene im Stream festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bac61-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="bac61-116">Die Verweis Werte sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bac61-116">The reference values are read-only.</span></span> <span data-ttu-id="bac61-117">Die Zielwerte werden von Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen für die dynamische Bereichs Kontrolle des Benutzers aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="bac61-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="bac61-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bac61-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac61-119">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="bac61-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="bac61-120">**WM/wmadrcaveragereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="bac61-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="bac61-121">**WM/wmadrcaveragetarget**</span><span class="sxs-lookup"><span data-stu-id="bac61-121">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="bac61-122">**WM/wmadrcpeer Reference**</span><span class="sxs-lookup"><span data-stu-id="bac61-122">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> </dl>

 

 




