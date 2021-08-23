---
description: Digitale Signalprozessoren
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Digitale Signalprozessoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f5c9aa0ee3c4cc2a8c7f725b3a8444f4852c8c5b52ee3713b533ec435f4a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100942"
---
# <a name="digital-signal-processors"></a>Digitale Signalprozessoren

In diesem Abschnitt werden die DSP-Objekte (Digital Signal Processor) beschrieben, die von Windows.

Microsoft verwendet den Begriff Digitale *Signalprozessor,* um eine Reihe von COM-Objekten zu bestimmen, die Transformationen für unkomprimierte Audio- und Videodaten durchführen. Die in diesem SDK beschriebenen DSPs transformieren Audio- und Videodaten in eine Vielzahl von unkomprimierten Formaten.

Die DSPs können selbst oder in Kombination mit Audio- und Videocodecs verwendet werden. Mit Ausnahme des Voice Capture-DSP implementiert jeder hier aufgeführte DSP zwei separate, aber ähnliche Schnittstellen.



| Schnittstelle                              | Beschreibung                                 |
|----------------------------------------|---------------------------------------------|
| [**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Kompatibel mit Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Kompatibel mit DirectShow.                 |



 

Sie können die DSPs konfigurieren, indem Sie die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) zum Festlegen von Eigenschaften verwenden. Einige der DSPs verfügen über zusätzliche Schnittstellen, die Eigenschaften festlegen. Um diese Schnittstellen zu verwenden, rufen Sie die [**QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) einer beliebigen anderen Schnittstelle des DSP auf. Das Referenzthema für jeden DSP listet die unterstützten Eigenschaften, Schnittstellen und andere Features auf.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Dsp                                                      | Beschreibung                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [Audio Resampler DSP](audioresampler.md)                | Konvertiert die Samplingrate eines Audiostreams.       |
| [Farbsteuerungstransformations-DSP](colorcontroltransform.md) | Passt die Farbmerkmale eines Videostreams an. |
| [Farbkonverter-DSP](colorconverter.md)                | Konvertiert einen Videostream zwischen Farbformaten.       |
| [Bildfrequenzkonverter-DSP](framerateconverter.md)       | Ändert die Bildfrequenz eines Videostreams.            |
| [Video Resizer DSP](videoresizer.md)                    | Ändern der Größe eines Videostreams.                              |
| [Voice Capture-DSP](voicecapturedmo.md)                 | Kapselt mehrere DSPs im Zusammenhang mit der Spracherfassung.  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierreferenz](media-foundation-programming-reference.md)
</dt> </dl>

 

 
