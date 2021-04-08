---
description: Verwenden von decimations zur Optimierung der Mischungs Leistung
ms.assetid: 94d4ce86-9d60-4fd4-ab01-851dc073680b
title: Verwenden von decimations zur Optimierung der Mischungs Leistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e9e4ddfe3bbba3eb5eeab91b7cf0e8b9cbfa03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866459"
---
# <a name="using-decimation-to-optimize-mixing-performance"></a><span data-ttu-id="fd8dc-103">Verwenden von decimations zur Optimierung der Mischungs Leistung</span><span class="sxs-lookup"><span data-stu-id="fd8dc-103">Using Decimation to Optimize Mixing Performance</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd8dc-104">Die in diesem Abschnitt beschriebene Optimierung hängt stark von der zugrunde liegenden Hardware ab.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-104">The optimization described in this section is highly dependent on the underlying hardware.</span></span> <span data-ttu-id="fd8dc-105">Wenn Sie nicht garantieren können, welche Art von Grafikhardware mit der Anwendung verwendet wird, kann die Darstellung des Video Bilds erheblich beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-105">Unless you can guarantee what type of graphics hardware will be used with the application, it may seriously degrade the appearance of the video image.</span></span>

 

<span data-ttu-id="fd8dc-106">Für den Prozessor ist eine hohe Verarbeitungsleistung erforderlich, die auf neueren Systemen größtenteils von der Grafikkarte bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-106">HDTV requires a lot of processing power, which on newer systems is provided mostly by the graphics card.</span></span> <span data-ttu-id="fd8dc-107">Auch wenn die Grafikkarte und der Decoder Auflösungen von 1920 x 1080 unterstützen können, ist der Benutzer möglicherweise nicht immer auf diese Lösung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-107">But even if the graphics card and the decoder can support resolutions of 1920x1080, the user may not always have their monitor set to this resolution.</span></span> <span data-ttu-id="fd8dc-108">In diesem Fall ist der Grafikchip erforderlich, um ein 1920 x 1080-Abbild zu erstellen und dann die Auflösung zu verringern, bevor es an den Frame Puffer gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-108">In this case, the graphics chip is required to create a 1920 x 1080 image, and then reduce the resolution before sending it to the frame buffer.</span></span>

<span data-ttu-id="fd8dc-109">Da dies eine Verschwendung der Verarbeitungsleistung darstellt, bietet VMR eine Möglichkeit, das Bild zu dem Zeitpunkt zu dezimieren (zu verringern), zu dem es auf der DirectDraw-Oberfläche gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-109">Since this is a waste of processing power, the VMR provides a way to decimate (reduce) the image at the time it is being rendered onto the DirectDraw surface.</span></span> <span data-ttu-id="fd8dc-110">Dadurch entfällt die zusätzliche Speicher Kopie, die erforderlich ist, wenn die Größe des Abbilds geändert werden muss, nachdem es gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-110">This eliminates the extra memory copy required if the image has to be resized after it has been rendered.</span></span>

<span data-ttu-id="fd8dc-111">**VMR-7:** Um die Dezimaltrennzeichen zu aktivieren, rufen Sie [**ivmrmixercontrol:: setmixingprefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) mit dem mixerpref \_ decimateoutput-Flag auf.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-111">**VMR-7:** To enable decimation, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_DecimateOutput flag.</span></span>

<span data-ttu-id="fd8dc-112">**VMR-9:** Um Decimation zu aktivieren, rufen Sie [**IVMRMixerControl9:: setmixingprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) mit dem MixerPref9 \_ decimateoutput-Flag auf.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-112">**VMR-9:** To enable decimation, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_DecimateOutput flag.</span></span>

<span data-ttu-id="fd8dc-113">Die **setmixingprefs** -Methode muss aufgerufen werden, bevor die VMR verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-113">The **SetMixingPrefs** method must be called before the VMR is connected.</span></span> <span data-ttu-id="fd8dc-114">Die Mischungs Einstellungs Flags können nicht geändert werden, sobald das Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd8dc-114">The mixing preference flags cannot be changed once the graph is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd8dc-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fd8dc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd8dc-116">Verwenden des VMR-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="fd8dc-116">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



