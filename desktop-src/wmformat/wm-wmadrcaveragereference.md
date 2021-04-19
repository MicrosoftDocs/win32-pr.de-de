---
title: WM/wmadrcaveragereferenzierung
description: Das WM/wmadrcaveragereferenzierungsattribut enthält die durchschnittliche Volumeebene der Datei als codiert.
ms.assetid: 994614e3-06e2-48f0-bdac-6de5ab0c0eff
keywords:
- WM/wmadrcaveragereferenzierung Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMADRCAverageReference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7059b68658d070ca71a738a5e20658474139558
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341899"
---
# <a name="wmwmadrcaveragereference"></a><span data-ttu-id="f899a-104">WM/wmadrcaveragereferenzierung</span><span class="sxs-lookup"><span data-stu-id="f899a-104">WM/WMADRCAverageReference</span></span>

<span data-ttu-id="f899a-105">Das **WM/wmadrcaveragereferenzierungsattribut** enthält die durchschnittliche Volumeebene der Datei als codiert.</span><span class="sxs-lookup"><span data-stu-id="f899a-105">The **WM/WMADRCAverageReference** attribute contains the average volume level of the file as encoded.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f899a-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="f899a-106">Global Constant</span></span>

<span data-ttu-id="f899a-107">g \_ wszwmwmadrcaveragereferenzierung</span><span class="sxs-lookup"><span data-stu-id="f899a-107">g\_wszWMWMADRCAverageReference</span></span>

## <a name="data-type"></a><span data-ttu-id="f899a-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f899a-108">Data Type</span></span>

<span data-ttu-id="f899a-109">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f899a-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="f899a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f899a-110">Remarks</span></span>

<span data-ttu-id="f899a-111">Es gibt vier Attribute, die von Windows-Media Player für das dynamische Bereichs Steuerelement verwendet werden: **WM/wmadrcaveragereferenzierung**, **WM/wmadrcpeer Reference**, **WM/wmadrcaveragetarget** und **WM/wmadrcpeer Target**.</span><span class="sxs-lookup"><span data-stu-id="f899a-111">There are four attributes used by Windows Media Player for dynamic range control: **WM/WMADRCAverageReference**, **WM/WMADRCPeakReference**, **WM/WMADRCAverageTarget**, and **WM/WMADRCPeakTarget**.</span></span> <span data-ttu-id="f899a-112">Alle diese Werte werden vom Writer auf der Grundlage von Informationen aus dem Codec festgelegt, wenn Streams mit dem Windows Media Audio 9-Codec oder Windows Media Audio 9 Professional-Codec geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="f899a-112">All of these values are set by the writer based on information from the codec when writing streams with the Windows Media Audio 9 codec or Windows Media Audio 9 Professional codec.</span></span> <span data-ttu-id="f899a-113">Die durchschnittlichen Werte werden auf die durchschnittliche Volumeebene des Streams festgelegt, und die Spitzenwerte werden auf die maximale Volumeebene im Stream festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f899a-113">The average values are set to the average volume level of the stream, and the peak values are set to the maximum volume level in the stream.</span></span> <span data-ttu-id="f899a-114">Die Verweis Werte sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f899a-114">The reference values are read-only.</span></span> <span data-ttu-id="f899a-115">Die Zielwerte werden von Windows Media Player festgelegt, wenn die Datei wiedergegeben wird, um die Einstellungen für die dynamische Bereichs Kontrolle des Benutzers aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="f899a-115">The target values are set by Windows Media Player when the file is being played to record the dynamic range control preferences of the user.</span></span>

## <a name="see-also"></a><span data-ttu-id="f899a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f899a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f899a-117">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="f899a-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="f899a-118">**WM/wmadrcaveragetarget**</span><span class="sxs-lookup"><span data-stu-id="f899a-118">**WM/WMADRCAverageTarget**</span></span>](wm-wmadrcaveragetarget.md)
</dt> <dt>

[<span data-ttu-id="f899a-119">**WM/wmadrcpeer Reference**</span><span class="sxs-lookup"><span data-stu-id="f899a-119">**WM/WMADRCPeakReference**</span></span>](wm-wmadrcpeakreference.md)
</dt> <dt>

[<span data-ttu-id="f899a-120">**WM/wmadrcpeer Target**</span><span class="sxs-lookup"><span data-stu-id="f899a-120">**WM/WMADRCPeakTarget**</span></span>](wm-wmadrcpeaktarget.md)
</dt> </dl>

 

 




