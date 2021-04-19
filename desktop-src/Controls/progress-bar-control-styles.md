---
title: Statusanzeige-Steuerelement Stile (kommctrl. h)
description: Die folgenden Steuerelement Stile werden von Statusanzeige-Steuerelementen unterstützt.
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370081"
---
# <a name="progress-bar-control-styles"></a><span data-ttu-id="aec3e-103">Stile der Statusanzeige-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="aec3e-103">Progress Bar Control Styles</span></span>

<span data-ttu-id="aec3e-104">Die folgenden Steuerelement Stile werden von den [Status](progress-bar-control.md) Anzeige-Steuerelementen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="aec3e-104">The following control styles are supported by [Progress Bar](progress-bar-control.md) controls:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="aec3e-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="aec3e-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="aec3e-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aec3e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <span data-ttu-id="aec3e-107"><dt><strong>PBS_MARQUEE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aec3e-107"><dt><strong>PBS_MARQUEE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aec3e-108"><a href="common-control-versions.md">Version 6,0</a> oder höher.</span><span class="sxs-lookup"><span data-stu-id="aec3e-108"><a href="common-control-versions.md">Version 6.0</a> or later.</span></span> <span data-ttu-id="aec3e-109">Der Status Indikator vergrößert sich nicht in der Größe, sondern verschiebt sich wiederholt entlang der Länge des Balkens, was die Aktivität angibt, ohne anzugeben, welcher Anteil des Fortschritts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="aec3e-109">The progress indicator does not grow in size but instead moves repeatedly along the length of the bar, indicating activity without specifying what proportion of the progress is complete.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aec3e-110">Comctl32.dll Version 6 ist nicht Verteil Bar, aber in Windows oder höher enthalten.</span><span class="sxs-lookup"><span data-stu-id="aec3e-110">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="aec3e-111">Wenn Sie Comctl32.dll Version 6 verwenden möchten, geben Sie ihn in einem Manifest an.</span><span class="sxs-lookup"><span data-stu-id="aec3e-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="aec3e-112">Weitere Informationen zu Manifesten finden Sie unter <a href="cookbook-overview.md">Aktivieren von visuellen Stilen</a>.</span><span class="sxs-lookup"><span data-stu-id="aec3e-112">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <span data-ttu-id="aec3e-113"><dt><strong>PBS_SMOOTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aec3e-113"><dt><strong>PBS_SMOOTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aec3e-114"><a href="common-control-versions.md">Version 4,70</a> oder höher.</span><span class="sxs-lookup"><span data-stu-id="aec3e-114"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="aec3e-115">In der Statusleiste wird der Status Status in einer Smooth Scrollleiste anstelle der standardmäßigen segmentierten Leiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aec3e-115">The progress bar displays progress status in a smooth scrolling bar instead of the default segmented bar.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aec3e-116">Dieser Stil wird nur im klassischen Windows-Design unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aec3e-116">This style is supported only in the Windows Classic theme.</span></span> <span data-ttu-id="aec3e-117">Alle anderen Designs überschreiben diesen Stil.</span><span class="sxs-lookup"><span data-stu-id="aec3e-117">All other themes override this style.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <span data-ttu-id="aec3e-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aec3e-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aec3e-119"><a href="common-control-versions.md">Version 6,0</a> oder höher und <strong>Windows Vista.</strong></span><span class="sxs-lookup"><span data-stu-id="aec3e-119"><a href="common-control-versions.md">Version 6.0</a> or later and <strong>Windows Vista.</strong></span></span> <span data-ttu-id="aec3e-120">Bestimmt das Animations Verhalten, das von der Statusanzeige bei Rückwärtsbewegung (von einem höheren zu einem niedrigeren Wert) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aec3e-120">Determines the animation behavior that the progress bar should use when moving backward (from a higher value to a lower value).</span></span> <span data-ttu-id="aec3e-121">Wenn dies festgelegt ist, &quot; wird ein reibungsloser &quot; Übergang ausgeführt, andernfalls springt das Steuerelement &quot; &quot; zum niedrigeren Wert.</span><span class="sxs-lookup"><span data-stu-id="aec3e-121">If this is set, then a &quot;smooth&quot; transition will occur, otherwise the control will &quot;jump&quot; to the lower value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <span data-ttu-id="aec3e-122"><dt><strong>PBS_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="aec3e-122"><dt><strong>PBS_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="aec3e-123"><a href="common-control-versions.md">Version 4,70</a> oder höher.</span><span class="sxs-lookup"><span data-stu-id="aec3e-123"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="aec3e-124">In der Statusleiste wird der Status vertikal von unten nach oben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aec3e-124">The progress bar displays progress status vertically, from bottom to top.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="aec3e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aec3e-125">Remarks</span></span>

<span data-ttu-id="aec3e-126">Sie können die Stile der Statusanzeige auf die gleiche Weise wie andere gängige Steuerelemente mit "", " [**", "**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)", " [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)" oder " [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)" festlegen.</span><span class="sxs-lookup"><span data-stu-id="aec3e-126">You can set progress bar styles, in the same way as other common controls, with [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga), or [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="aec3e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aec3e-127">Requirements</span></span>



| <span data-ttu-id="aec3e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aec3e-128">Requirement</span></span> | <span data-ttu-id="aec3e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="aec3e-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aec3e-130">Header</span><span class="sxs-lookup"><span data-stu-id="aec3e-130">Header</span></span><br/> | <dl> <span data-ttu-id="aec3e-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="aec3e-131"><dt>CommCtrl.h</dt></span></span> </dl> |



 

