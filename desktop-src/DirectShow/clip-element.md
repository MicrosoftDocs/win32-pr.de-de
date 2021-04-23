---
description: Der Clip gibt eine Medienquelle an.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: clip-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d937f942ba7b564e65b0e37d9c11929805287da
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908668"
---
# <a name="clip-element"></a><span data-ttu-id="75eb6-103">clip-Element</span><span class="sxs-lookup"><span data-stu-id="75eb6-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="75eb6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="75eb6-104">\[Deprecated.</span></span> <span data-ttu-id="75eb6-105">Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]</span><span class="sxs-lookup"><span data-stu-id="75eb6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="75eb6-106">Gibt `clip` eine Medienquelle an.</span><span class="sxs-lookup"><span data-stu-id="75eb6-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="75eb6-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="75eb6-107">Attributes</span></span>

<span data-ttu-id="75eb6-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="75eb6-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="75eb6-109">Informationen zu über- und untergeordneten Daten</span><span class="sxs-lookup"><span data-stu-id="75eb6-109">Parent/Child Information</span></span>



| <span data-ttu-id="75eb6-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="75eb6-110">Label</span></span> | <span data-ttu-id="75eb6-111">Wert</span><span class="sxs-lookup"><span data-stu-id="75eb6-111">Value</span></span> |
|----------|----------------------------------|
| <span data-ttu-id="75eb6-112">Parent</span><span class="sxs-lookup"><span data-stu-id="75eb6-112">Parent</span></span>   | [<span data-ttu-id="75eb6-113">**track**</span><span class="sxs-lookup"><span data-stu-id="75eb6-113">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="75eb6-114">Children</span><span class="sxs-lookup"><span data-stu-id="75eb6-114">Children</span></span> | [<span data-ttu-id="75eb6-115">**Wirkung**</span><span class="sxs-lookup"><span data-stu-id="75eb6-115">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="75eb6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75eb6-116">Remarks</span></span>

<span data-ttu-id="75eb6-117">Das **clsid-Attribut** gibt die CLSID eines Quellfilters an, der als Quelle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="75eb6-117">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="75eb6-118">Geben Sie die **Attribute src** und **clsid nicht** innerhalb desselben Elements `clip` an.</span><span class="sxs-lookup"><span data-stu-id="75eb6-118">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="75eb6-119">Geben Sie mindestens ein Startzeitattribut (**start** oder **mstart**) und ein Stoppzeitattribut (**stop** oder mstop ) **an.**</span><span class="sxs-lookup"><span data-stu-id="75eb6-119">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="75eb6-120">Wenn eines der Startzeitattribute nicht angegeben ist, wird standardmäßig 0 (der Anfang der Zeitachse für **start** oder der Anfang des Clips für **mstart ) verwendet.**</span><span class="sxs-lookup"><span data-stu-id="75eb6-120">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="75eb6-121">Wenn eines der Stoppzeitattribute nicht angegeben ist, geht DES von einer normalen Wiedergaberate aus und berechnet die nicht angegebene Stoppzeit entsprechend.</span><span class="sxs-lookup"><span data-stu-id="75eb6-121">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="75eb6-122">Wenn beide Stoppzeiten angegeben sind, ist die Wiedergabe bei Bedarf schneller oder langsamer als normal.</span><span class="sxs-lookup"><span data-stu-id="75eb6-122">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="75eb6-123">Im folgenden Beispiel beträgt die Zeitachse sieben Sekunden (**Stop** minus **Start**).</span><span class="sxs-lookup"><span data-stu-id="75eb6-123">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="75eb6-124">Es wird eine normale Wiedergaberate angenommen, sodass die Medienstoppzeit standardmäßig 10 Sekunden beträgt (Dauer plus **mstart).**</span><span class="sxs-lookup"><span data-stu-id="75eb6-124">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="75eb6-125">Im nächsten Beispiel wird die Medienstartzeit standardmäßig auf 0 festgelegt, sodass die Mediendauer 10 Sekunden beträgt.</span><span class="sxs-lookup"><span data-stu-id="75eb6-125">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="75eb6-126">Die Dauer der Zeitachse beträgt fünf Sekunden, sodass der Clip doppelt so schnell wie gewohnt abspielt.</span><span class="sxs-lookup"><span data-stu-id="75eb6-126">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="75eb6-127">Wenn das **src-Attribut** ein Stillbild angibt, versucht DES, eine Reihe von Still-Bildern zu laden, um eine Animation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="75eb6-127">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="75eb6-128">Wenn das **src-Attribut** beispielsweise IMAGE001.BMP ist, sucht DES nach IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP usw.</span><span class="sxs-lookup"><span data-stu-id="75eb6-128">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="75eb6-129">Wenn sie vorhanden sind, werden sie in sequenzieller numerischer Reihenfolge mit der vom **Framerate-Attribut** angegebenen Rate angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75eb6-129">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="75eb6-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75eb6-130">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="75eb6-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="75eb6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75eb6-132">XTL-Elemente</span><span class="sxs-lookup"><span data-stu-id="75eb6-132">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



