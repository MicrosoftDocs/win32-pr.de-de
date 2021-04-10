---
description: Informationen zum audioerfassungs Filter
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Informationen zum audioerfassungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125281"
---
# <a name="about-the-audio-capture-filter"></a><span data-ttu-id="8bc5b-103">Informationen zum audioerfassungs Filter</span><span class="sxs-lookup"><span data-stu-id="8bc5b-103">About the Audio Capture Filter</span></span>

<span data-ttu-id="8bc5b-104">DirectShow ermöglicht die Erfassung aus den analogen Eingaben auf einer Soundkarte über den [audioerfassungs Filter](audio-capture-filter.md).</span><span class="sxs-lookup"><span data-stu-id="8bc5b-104">DirectShow enables capture from the analog inputs on a sound card through the [Audio Capture Filter](audio-capture-filter.md).</span></span> <span data-ttu-id="8bc5b-105">Dieser Filter verwendet die WaveIn *xxx* -APIs, um jedes Gerät zu steuern, dessen Treiber diese APIs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-105">This filter uses the waveIn *XXX* APIs to control any device whose driver supports these APIs.</span></span> <span data-ttu-id="8bc5b-106">Jede Karte im System wird durch eine separate Instanz des Filters dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-106">Each card on the system is represented by a separate instance of the filter.</span></span>

<span data-ttu-id="8bc5b-107">Der audioerfassungs Filter macht jede Eingabe auf der Karte (z. b. das Mikrofon oder die Eingabe-PIN) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-107">The Audio Capture filter exposes each input on the card, such as the microphone or the MIDI input, as an input pin.</span></span> <span data-ttu-id="8bc5b-108">Die Eingabe Pins stellen dar, was der Treiber als audioquellzeilen verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-108">The input pins represent what the driver exposes as audio source lines.</span></span> <span data-ttu-id="8bc5b-109">Es werden jedoch keine Daten durch diese Eingabe Pins durchlaufen, und Sie stellen keine Verbindung mit anderen DirectShow-Filtern her.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-109">No data travels through these input pins, however, and they do not connect to other DirectShow filters.</span></span> <span data-ttu-id="8bc5b-110">Sie bieten lediglich eine Möglichkeit für eine Anwendung, die Eingaben zu steuern.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-110">They simply provide a way for an application to control the inputs.</span></span> <span data-ttu-id="8bc5b-111">Die Anwendung kann eine Eingabe-PIN verwenden, um die Eingabe zu aktivieren oder zu deaktivieren, oder um Mischungs Eigenschaften wie z. b. Bass-Ausgleich, Höhen-Ausgleich, Pan usw. festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-111">The application can use an input pin to enable or disable the input, or to set mixing properties such as bass equalization, treble equalization, pan, and so forth.</span></span> <span data-ttu-id="8bc5b-112">Der verfügbare Steuerungs Umfang hängt vom Treiber ab.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-112">The amount of control that is available depends on the driver.</span></span> <span data-ttu-id="8bc5b-113">Um die Funktionen einer bestimmten Soundkarte vollständig zu verstehen und auszunutzen, benötigen Sie die Dokumentation des Herstellers der Karte.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-113">To fully understand and exploit the capabilities of a particular sound card, you will need the documentation from the card's manufacturer.</span></span>

> [!Note]  
> <span data-ttu-id="8bc5b-114">Sie können eine Erfassung aus den CD-Audio Eingaben durchführen, aber dieser Audiostream wurde bereits über den Digital-to-Analog-Konverter durchlaufen, sodass es zu einem Verlust der Soundqualität von der ursprünglichen CD kommt.</span><span class="sxs-lookup"><span data-stu-id="8bc5b-114">You can capture from the CD-Audio input, but this audio stream has already gone through the digital-to-analog converter, so there will be a loss of sound quality from the original CD.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8bc5b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8bc5b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bc5b-116">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="8bc5b-116">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



