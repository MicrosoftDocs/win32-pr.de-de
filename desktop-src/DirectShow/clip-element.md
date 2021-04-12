---
description: Der Clip gibt eine Medienquelle an.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Clip-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480995"
---
# <a name="clip-element"></a><span data-ttu-id="915d2-103">Clip-Element</span><span class="sxs-lookup"><span data-stu-id="915d2-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="915d2-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="915d2-104">\[Deprecated.</span></span> <span data-ttu-id="915d2-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="915d2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="915d2-106">Der ermittelt `clip` eine Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="915d2-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="915d2-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="915d2-107">Attributes</span></span>

<span data-ttu-id="915d2-108">[**CLSID**](clsid-attribute.md), [**Framerate**](framerate-attribute.md), [**Lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstopps**](mstop-attribute.md), [**stumm**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [](stop-attribute.md)Start, [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="915d2-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="915d2-109">Über-/unterordnungsinformationen</span><span class="sxs-lookup"><span data-stu-id="915d2-109">Parent/Child Information</span></span>



|          |                                  |
|----------|----------------------------------|
| <span data-ttu-id="915d2-110">Parent</span><span class="sxs-lookup"><span data-stu-id="915d2-110">Parent</span></span>   | [<span data-ttu-id="915d2-111">**track**</span><span class="sxs-lookup"><span data-stu-id="915d2-111">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="915d2-112">Children</span><span class="sxs-lookup"><span data-stu-id="915d2-112">Children</span></span> | [<span data-ttu-id="915d2-113">**entsprechende**</span><span class="sxs-lookup"><span data-stu-id="915d2-113">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="915d2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="915d2-114">Remarks</span></span>

<span data-ttu-id="915d2-115">Das **CLSID** -Attribut gibt die CLSID eines Quell Filters an, der als Quelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="915d2-115">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="915d2-116">Geben Sie die Attribute **src** und **CLSID** nicht innerhalb desselben `clip` Elements an.</span><span class="sxs-lookup"><span data-stu-id="915d2-116">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="915d2-117">Geben Sie mindestens ein Start Zeit Attribut ("**Start** " oder " **mstart**") und ein Attribut für die Beendigung an ("**Ende** " oder " **mstoppzeit**").</span><span class="sxs-lookup"><span data-stu-id="915d2-117">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="915d2-118">Wenn eines der Start Zeit Attribute nicht angegeben ist, wird es standardmäßig auf 0 (den Anfang der Zeitachse für **Start** oder den Anfang des Clips für **mstart**) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="915d2-118">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="915d2-119">Wenn eines der Attribute für die Endzeit nicht angegeben ist, nimmt des eine normale Wiedergabe Rate an und berechnet die nicht angegebene Endzeit entsprechend.</span><span class="sxs-lookup"><span data-stu-id="915d2-119">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="915d2-120">Wenn beide Endzeiten angegeben sind, ist die Wiedergabe bei Bedarf schneller oder langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="915d2-120">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="915d2-121">Im folgenden Beispiel beträgt die Zeitachsen Dauer sieben Sekunden (**Ende** minus **Start**).</span><span class="sxs-lookup"><span data-stu-id="915d2-121">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="915d2-122">Es wird davon ausgegangen, dass die Standard Wiedergabe Rate standardmäßig 10 Sekunden beträgt (die Dauer Plus **mstart**).</span><span class="sxs-lookup"><span data-stu-id="915d2-122">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="915d2-123">Im nächsten Beispiel wird die Start Zeit der Medien standardmäßig auf 0 (null) eingestellt und die Dauer des Mediums auf 10 Sekunden erzwungen.</span><span class="sxs-lookup"><span data-stu-id="915d2-123">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="915d2-124">Die Zeitachsen Dauer beträgt fünf Sekunden, sodass der Clip mit der doppelten Geschwindigkeit wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="915d2-124">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="915d2-125">Wenn das **src** -Attribut ein immer noch Bild angibt, versucht des, eine Reihe von Bildern zu laden, um eine Animation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="915d2-125">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="915d2-126">Wenn das **src** -Attribut z. b. IMAGE001.BMP ist, sucht des nach IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP usw.</span><span class="sxs-lookup"><span data-stu-id="915d2-126">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="915d2-127">Wenn Sie vorhanden sind, werden Sie in sequenzieller numerischer Reihenfolge mit dem vom **Framerate** -Attribut angegebenen Satz angezeigt.</span><span class="sxs-lookup"><span data-stu-id="915d2-127">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="915d2-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="915d2-128">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="915d2-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="915d2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915d2-130">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="915d2-130">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



