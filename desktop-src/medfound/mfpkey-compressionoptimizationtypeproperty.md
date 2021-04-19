---
description: Gibt die optimalen Einstellungen für die visuelle Qualität an, die für den erweiterten Windows Media Video 9-Profil Encoder verwendet werden sollen.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348320"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a><span data-ttu-id="77661-103">Mfpkey \_ compressionoptimizationtype (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="77661-103">MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE Property</span></span>

<span data-ttu-id="77661-104">Gibt die optimalen Einstellungen für die visuelle Qualität an, die für den erweiterten Windows Media Video 9-Profil Encoder verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="77661-104">Specifies the optimal visual quality settings to use for the Windows Media Video 9 Advanced Profile encoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="77661-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="77661-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="77661-106">g \_ wszwmvccompressionoptimizationtype</span><span class="sxs-lookup"><span data-stu-id="77661-106">g\_wszWMVCCompressionOptimizationType</span></span>

## <a name="data-type"></a><span data-ttu-id="77661-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="77661-107">Data Type</span></span>

<span data-ttu-id="77661-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="77661-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="77661-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="77661-109">Default Value</span></span>

<span data-ttu-id="77661-110">0</span><span class="sxs-lookup"><span data-stu-id="77661-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="77661-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77661-111">Remarks</span></span>

<span data-ttu-id="77661-112">Diese Eigenschaft bietet eine schnelle Möglichkeit, eine Reihe von Optionen für die Videocodierung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="77661-112">This property provides a quick way to configure a number of video encoding options.</span></span> <span data-ttu-id="77661-113">Sie kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="77661-113">It may be set to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="77661-114">Wert</span><span class="sxs-lookup"><span data-stu-id="77661-114">Value</span></span></th>
<th><span data-ttu-id="77661-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="77661-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="77661-116">0</span><span class="sxs-lookup"><span data-stu-id="77661-116">0</span></span></td>
<td><span data-ttu-id="77661-117">Der Codec erzwingt keine Optimierung und verwendet alle Funktionen, die von anderen Eigenschaften angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77661-117">The codec will not force optimization and will use whatever features are specified by other properties.</span></span> <span data-ttu-id="77661-118">In vielen Fällen verwendet der Codec interne Logik, um Einstellungen zu ermitteln, wenn Sie nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="77661-118">In many cases, the codec will use internal logic to determine settings if they are not specified.</span></span> <span data-ttu-id="77661-119">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="77661-119">This is the default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="77661-120">1</span><span class="sxs-lookup"><span data-stu-id="77661-120">1</span></span></td>
<td><span data-ttu-id="77661-121">Aktiviert die Funktionen, mit denen die beste visuelle Qualität erzeugt wird. Wenn Sie diesen Wert verwenden, wird der Codec so konfiguriert, als hätten Sie die folgenden Eigenschaften festgelegt:</span><span class="sxs-lookup"><span data-stu-id="77661-121">Enables the features that will produce the best visual quality.Using this value configures the codec as if you had set the following properties:</span></span><br/>
<ul>
<li><span data-ttu-id="77661-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span><span class="sxs-lookup"><span data-stu-id="77661-122"><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</span></span></li>
<li><span data-ttu-id="77661-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span><span class="sxs-lookup"><span data-stu-id="77661-123"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</span></span></li>
<li><span data-ttu-id="77661-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span><span class="sxs-lookup"><span data-stu-id="77661-124"><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</span></span></li>
<li><span data-ttu-id="77661-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</span><span class="sxs-lookup"><span data-stu-id="77661-125"><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</span></span></li>
<li><span data-ttu-id="77661-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span><span class="sxs-lookup"><span data-stu-id="77661-126"><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</span></span></li>
<li><span data-ttu-id="77661-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</span><span class="sxs-lookup"><span data-stu-id="77661-127"><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</span></span></li>
<li><span data-ttu-id="77661-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span><span class="sxs-lookup"><span data-stu-id="77661-128"><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</span></span></li>
</ul>
<span data-ttu-id="77661-129">Wenn Sie eine der Eigenschaften in der vorherigen Liste festlegen, überschreibt der von Ihnen festgelegte Wert die Werte, die dieser Einstellung zugeordnet sind, mit Ausnahme der <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="77661-129">If you set any of the properties in the previous list, the value you set overrides the values associated with this setting, except for <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="77661-130">Wenn Sie den Wert der \_ Eigenschaft "compressionoptimizationtype" der Eigenschaft "mfpkey" auf "1" festlegen, wirkt sich dies auch auf "2" und die Registrierungs Einstellung der Bewegungsvektor-kostenmethode auf "1" aus.</span><span class="sxs-lookup"><span data-stu-id="77661-130">Setting the value of the MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE property to 1 also has the effect of setting the Dquant Option registry setting to 2, and the Motion Vector Cost Method registry setting to 1.</span></span> <span data-ttu-id="77661-131">Weitere Informationen finden Sie im Webartikel [using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span><span class="sxs-lookup"><span data-stu-id="77661-131">For more information, see the web article [Using the Advanced Settings of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="77661-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77661-132">Requirements</span></span>



| <span data-ttu-id="77661-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77661-133">Requirement</span></span> | <span data-ttu-id="77661-134">Wert</span><span class="sxs-lookup"><span data-stu-id="77661-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="77661-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77661-135">Minimum supported client</span></span><br/> | <span data-ttu-id="77661-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77661-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="77661-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77661-137">Minimum supported server</span></span><br/> | <span data-ttu-id="77661-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77661-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="77661-139">Header</span><span class="sxs-lookup"><span data-stu-id="77661-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="77661-140"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77661-140"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77661-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77661-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77661-142">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="77661-142">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




