---
description: Schnittstellen für Audioerfassung und-Rendering
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Schnittstellen für Audioerfassung und-Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f941c1220f1adc06a686d702e9db21095a8cb7e6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343570"
---
# <a name="audio-capture-and-rendering-interfaces"></a><span data-ttu-id="97b1d-103">Schnittstellen für Audioerfassung und-Rendering</span><span class="sxs-lookup"><span data-stu-id="97b1d-103">Audio Capture and Rendering Interfaces</span></span>

<span data-ttu-id="97b1d-104">Diese Schnittstellen unterstützen Audioerfassung und Rendering in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="97b1d-104">These interfaces support audio capture and rendering in DirectShow</span></span>



| <span data-ttu-id="97b1d-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="97b1d-105">Interface</span></span>                                              | <span data-ttu-id="97b1d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97b1d-106">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97b1d-107">**IAMAudioInputMixer**</span><span class="sxs-lookup"><span data-stu-id="97b1d-107">**IAMAudioInputMixer**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | <span data-ttu-id="97b1d-108">Greifen Sie auf die analogen Eingaben auf der Soundkarte des Systems zu, und passen Sie die Merkmale an, wie z. b. Mono oder Stereo, Mischungs Ebene, Schwenk Pegel, Lautstärke, Treble und Bass.</span><span class="sxs-lookup"><span data-stu-id="97b1d-108">Access the analog inputs on the system's sound card and adjust characteristics, such as mono or stereo, mix level, pan level, loudness, treble, and bass.</span></span> |
| [<span data-ttu-id="97b1d-109">**Iamaudiorendererstats**</span><span class="sxs-lookup"><span data-stu-id="97b1d-109">**IAMAudioRendererStats**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | <span data-ttu-id="97b1d-110">Erhalten Sie statistische Leistungsinformationen über das audiorendering.</span><span class="sxs-lookup"><span data-stu-id="97b1d-110">Get statistical performance information about audio renderering.</span></span>                                                                                          |
| [<span data-ttu-id="97b1d-111">**Iambufferaushandlung**</span><span class="sxs-lookup"><span data-stu-id="97b1d-111">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | <span data-ttu-id="97b1d-112">Steuern Sie, wie der audioerfassungs Filter Puffer ordnet.</span><span class="sxs-lookup"><span data-stu-id="97b1d-112">Control how the audio capture filter allocates buffers.</span></span>                                                                                                   |
| [<span data-ttu-id="97b1d-113">**Iamclockslave**</span><span class="sxs-lookup"><span data-stu-id="97b1d-113">**IAMClockSlave**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | <span data-ttu-id="97b1d-114">Steuern der Toleranz eines audiorenderers, wenn er mit einer anderen Uhr übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="97b1d-114">Control the tolerance of an audio renderer when it matches rates with another clock.</span></span>                                                                      |
| [<span data-ttu-id="97b1d-115">**Iamdirectsound**</span><span class="sxs-lookup"><span data-stu-id="97b1d-115">**IAMDirectSound**</span></span>](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | <span data-ttu-id="97b1d-116">Ermöglicht es einer Anwendung, anzugeben, welches Fenster den Fokus hat, um die DirectSound-Audiowiedergabe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="97b1d-116">Enables an application to specify which window has focus for controlling DirectSound audio playback.</span></span>                                                      |
| [<span data-ttu-id="97b1d-117">**Iamresourcecontrol**</span><span class="sxs-lookup"><span data-stu-id="97b1d-117">**IAMResourceControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | <span data-ttu-id="97b1d-118">Speichern Sie eine Ressource für Audiogeräte, bevor Sie benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="97b1d-118">Hold an audio device resource before it is needed.</span></span>                                                                                                        |
| [<span data-ttu-id="97b1d-119">**Iamstreamconfig**</span><span class="sxs-lookup"><span data-stu-id="97b1d-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | <span data-ttu-id="97b1d-120">Das Ausgabeformat des Erfassungs Filters wird abgefragt und festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97b1d-120">Query and set the capture filter's output format.</span></span>                                                                                                         |
| [<span data-ttu-id="97b1d-121">**Ibasicaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="97b1d-121">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | <span data-ttu-id="97b1d-122">Legen Sie audioausgabevolume und Saldo fest.</span><span class="sxs-lookup"><span data-stu-id="97b1d-122">Set audio output volume and balance.</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="97b1d-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="97b1d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97b1d-124">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="97b1d-124">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



