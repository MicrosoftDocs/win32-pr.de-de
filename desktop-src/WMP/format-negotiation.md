---
title: Aushandlung formatieren
description: Aushandlung formatieren
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Windows Media Player-Plug-ins, Format Aushandlung
- Plug-ins, Format Aushandlung
- Plug-Ins für die digitale Signalverarbeitung, Format Aushandlung
- DSP-Plug-ins, Format Aushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337603"
---
# <a name="format-negotiation"></a><span data-ttu-id="98279-107">Aushandlung formatieren</span><span class="sxs-lookup"><span data-stu-id="98279-107">Format Negotiation</span></span>

<span data-ttu-id="98279-108">Bei Windows Media Player und einem DSP-Plug-in für die gemeinsame Nutzung von Daten müssen beide Programme das Format der Daten, die Sie verarbeiten, zustimmen.</span><span class="sxs-lookup"><span data-stu-id="98279-108">For Windows Media Player and a DSP plug-in to share data, both programs must agree on the format of the data they are processing.</span></span> <span data-ttu-id="98279-109">Das DSP-Plug-in implementiert Methoden, die der Player aufruft, um zu bestimmen, welche Formate das Plug-in unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98279-109">The DSP plug-in implements methods that the Player calls to determine which formats the plug-in supports.</span></span> <span data-ttu-id="98279-110">Das Plug-in implementiert auch Methoden, die der Player aufruft, um das aktuelle Format festzulegen.</span><span class="sxs-lookup"><span data-stu-id="98279-110">The plug-in also implements methods that the Player calls to set the current format.</span></span>

<span data-ttu-id="98279-111">Wenn das Plug-in als "direkmo (direkmo)" fungiert, ermittelt Windows Media Player Medienformate und legt diese fest, indem Methoden der **imediaobject** -Schnittstelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="98279-111">If the plug-in is acting as a DirextX Media Object (DMO), Windows Media Player discovers and sets media formats by calling methods of the **IMediaObject** interface.</span></span> <span data-ttu-id="98279-112">Beispielsweise ruft der Player den **imediaobject:: getinputtype** des Plug-ins wiederholt auf, um eine Liste aller vom Plug-in unterstützten Eingabeformate zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98279-112">For example, the Player calls the plug-in's **IMediaObject::GetInputType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="98279-113">DMO-Plug-Ins verwenden die **DMO- \_ \_ Medientyp** Struktur zum Organisieren der Informationen, die ein Medienformat angeben.</span><span class="sxs-lookup"><span data-stu-id="98279-113">DMO plug-ins use the **DMO\_MEDIA\_TYPE** structure to organize the information that specifies a media format.</span></span> <span data-ttu-id="98279-114">Weitere Informationen zur Verwendung von DMO-Plug-ins und des playeraushandlungs-Formats finden Sie unter [Informationen zu imediaobject](about-imediaobject.md).</span><span class="sxs-lookup"><span data-stu-id="98279-114">For more information about how DMO plug-ins and the Player negotiate format, see [About IMediaObject](about-imediaobject.md).</span></span>

<span data-ttu-id="98279-115">Wenn das Plug-in als Media Foundation Transformation (MFT) fungiert, erkennt Windows Media Player Medienformate durch Aufrufen von Methoden der **imftransform** -Schnittstelle und legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="98279-115">If the plug-in is acting as a Media Foundation Transform (MFT), Windows Media Player discovers and sets media formats by calling methods of the **IMFTransform** interface.</span></span> <span data-ttu-id="98279-116">Beispielsweise ruft der Player den **imftransform:: getinputavailabletype** des Plug-ins wiederholt auf, um eine Liste aller vom Plug-in unterstützten Eingabeformate zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="98279-116">For example, the Player calls the plug-in's **IMFTransform::GetInputAvailableType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="98279-117">MFT-Plug-ins und der Player verwenden die **imfmediatype** -Schnittstelle zum organisieren und Austauschen von Formatinformationen.</span><span class="sxs-lookup"><span data-stu-id="98279-117">MFT plug-ins and the Player use the **IMFMediaType** interface to organize and exchange format information.</span></span>

<span data-ttu-id="98279-118">Windows Media Player verwendet ein audiodsp-Plug-in nur dann, wenn das Plug-in dieselbe bidirektiontiefe wie die wiedergegebene digitale Audiodatei unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98279-118">Windows Media Player will use an audio DSP plug-in only if the plug-in supports the same bit depth as the digital audio being played.</span></span> <span data-ttu-id="98279-119">Wenn die digitale Audiodatei beispielsweise 20-Bit ist, muss das Plug-in für die Verarbeitung von 20-Bit-Audiodaten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="98279-119">For instance, if the digital audio is 20-bit, the plug-in must be written to process 20-bit audio.</span></span> <span data-ttu-id="98279-120">Bei CD-Audiodaten müssen DSP-Plug-ins 20-Bit-Verarbeitung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98279-120">For CD audio, DSP plug-ins must support 20-bit processing.</span></span>

<span data-ttu-id="98279-121">Bei der formataushandlung von Multi-Channel-Inhalten auf einem Computer, der für die Verwendung mit Stereo Referenten konfiguriert ist, versucht Windows Media Player zuerst, mithilfe des vorhandenen Eingabe-und Ausgabeformats eine Verbindung zu einem audiodsp-Plug-in herzustellen, indem **imediaobject:: setinputtype** und **imediaobject:: setoutputtype** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="98279-121">During format negotiation of multi-channel content on a computer configured for use with stereo speakers, Windows Media Player first attempts to connect to an audio DSP plug-in using the existing input and output format by calling **IMediaObject::SetInputType** and **IMediaObject::SetOutputType**.</span></span> <span data-ttu-id="98279-122">Nach dieser anfänglichen Aushandlung listet der Spieler die Formate auf, die das Plug-in unterstützt, und versucht, die beste Format Kombination für den Player und das Plug-in auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="98279-122">Once this initial negotiation occurs, the Player then enumerates the formats the plug-in supports and attempts to negotiate the best format combination for the Player and the plug-in.</span></span> <span data-ttu-id="98279-123">Wenn das Plug-in bei der anfänglichen Aushandlung Stereo-Audiodaten (definiert durch eine **WaveFormatEx** -Struktur) als Eingabeformat annimmt und anschließend nur multikanalaudiodaten akzeptiert (definiert durch eine **WAVEFORMATEXTENSIBLE** -Struktur), stellt der Spieler multikanalaudiodaten als Eingabeformat für das Plug-in bereit.</span><span class="sxs-lookup"><span data-stu-id="98279-123">If the plug-in accepts stereo audio (defined by a **WAVEFORMATEX** structure) as the input format during the initial negotiation, and then subsequently accepts only multi-channel audio (defined by a **WAVEFORMATEXTENSIBLE** structure), the Player will provide multi-channel audio as the input format to the plug-in.</span></span> <span data-ttu-id="98279-124">Dieses Verhalten während der formataushandlung ist für die Verwendung im Microsoft Windows XP-Betriebssystem verfügbar.</span><span class="sxs-lookup"><span data-stu-id="98279-124">This behavior during format negotiation is available for use in the Microsoft Windows XP operating system.</span></span> <span data-ttu-id="98279-125">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="98279-125">It may be altered or unavailable in subsequent versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98279-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98279-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98279-127">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="98279-127">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




