---
title: WM/wmadrcaveragetarget
description: Das WM/wmadrcaveragetarget-Attribut enthält die durchschnittliche Volumeebene, die vom Benutzer angefordert wurde. Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet.
ms.assetid: 8173b5ab-27e4-4af9-aea8-6c1310f065f5
keywords:
- WM/wmadrcaveragetarget-Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageTarget
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 387eed9112e8e0d79943b99bf326b07f42f425d1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339459"
---
# <a name="wmwmadrcaveragetarget"></a><span data-ttu-id="ba247-105">WM/wmadrcaveragetarget</span><span class="sxs-lookup"><span data-stu-id="ba247-105">WM/WMADRCAverageTarget</span></span>

<span data-ttu-id="ba247-106">Das **WM/wmadrcaveragetarget-** Attribut enthält die durchschnittliche Volumeebene, die vom Benutzer angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba247-106">The **WM/WMADRCAverageTarget** attribute contains the average volume level requested by the user.</span></span> <span data-ttu-id="ba247-107">Dieser Wert wird von Windows Media Player für die dynamische Bereichs Steuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba247-107">This value is used by Windows Media Player for dynamic range control.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ba247-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="ba247-108">Global Constant</span></span>

<span data-ttu-id="ba247-109">g \_ wszwmwmadrcaveragetarget</span><span class="sxs-lookup"><span data-stu-id="ba247-109">g\_wszWMWMADRCAverageTarget</span></span>

## <a name="data-type"></a><span data-ttu-id="ba247-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ba247-110">Data Type</span></span>

<span data-ttu-id="ba247-111">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ba247-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="ba247-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba247-112">Remarks</span></span>

<span data-ttu-id="ba247-113">Es gibt vier Attribute, die von Windows-Media Player für das dynamische Bereichs Steuerelement verwendet werden: **WM/wmadrcaveragereferenzierung**, **WM/wmadrcpeer Reference**, **WM/wmadrcaveragetarget** und **WM/wmadrcpeer Target**.</span><span class="sxs-lookup"><span data-stu-id="ba247-113">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="ba247-114">Alle diese Werte werden vom Writer auf der Grundlage von Informationen aus dem Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional-Codec geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ba247-114">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="ba247-115">Die durchschnittlichen Werte werden auf die durchschnittliche Volumeebene des Streams festgelegt, und die Spitzenwerte werden auf die maximale Volumeebene im Stream festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ba247-115">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="ba247-116">Die Verweis Werte sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ba247-116">The reference values are read-only.</span></span> <span data-ttu-id="ba247-117">Die Zielwerte werden von Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen für die dynamische Bereichs Kontrolle des Benutzers aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="ba247-117">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba247-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba247-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba247-119">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="ba247-119">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="ba247-120">**WM/wmadrcaveragereferenzierung**</span><span class="sxs-lookup"><span data-stu-id="ba247-120">**WM/WMADRCAverageReference**</span></span>](wm-wmadrcaveragereference.md)
</dt> <dt>

[<span data-ttu-id="ba247-121">**WM/wmadrcpeer Reference**</span><span class="sxs-lookup"><span data-stu-id="ba247-121">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="ba247-122">**WM/wmadrcpeer Target**</span><span class="sxs-lookup"><span data-stu-id="ba247-122">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




