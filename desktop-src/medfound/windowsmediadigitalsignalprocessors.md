---
description: Digitale Signal Prozessoren
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Digitale Signal Prozessoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106373415"
---
# <a name="digital-signal-processors"></a>Digitale Signal Prozessoren

In diesem Abschnitt werden die von Windows bereitgestellten DSP-Objekte (Digital Signal Processor) beschrieben.

Microsoft verwendet den Begriff *Digital Signal Processor* zum Festlegen eines Satzes von COM-Objekten, die Transformationen für nicht komprimierte Audiodaten und Videodaten ausführen. Die in diesem SDK beschriebenen DSPs transformieren Audiodaten und Videos in einer Vielzahl von unkomprimierten Formaten.

Die DSPs können eigenständig oder in Kombination mit Audio-und Video Codecs verwendet werden. Mit Ausnahme von "Voice Capture DSP" implementiert jeder hier aufgeführte DSP zwei separate, aber ähnliche Schnittstellen.



| Schnittstelle                              | BESCHREIBUNG                                 |
|----------------------------------------|---------------------------------------------|
| [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Kompatibel mit Microsoft Media Foundation. |
| [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Kompatibel mit DirectShow.                 |



 

Sie können die DSPs konfigurieren, indem Sie die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle verwenden, um Eigenschaften festzulegen. Einige der DSPs verfügen über zusätzliche Schnittstellen, die Eigenschaften festlegen. Um diese Schnittstellen zu verwenden, nennen Sie die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode einer beliebigen anderen Schnittstelle des DSP. Das Referenz Thema für die einzelnen DSP listet die unterstützten Eigenschaften, Schnittstellen und andere Funktionen auf.

In diesem Abschnitt werden die folgenden Themen behandelt:



| DSP                                                      | BESCHREIBUNG                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [Audioresampler-DSP](audioresampler.md)                | Konvertiert die Samplingrate eines Audiodatenstroms.       |
| [Farb Steuerungs Transformation (DSP)](colorcontroltransform.md) | Passt die Farbmerkmale eines Videostreams an. |
| [Farb Konverter-DSP](colorconverter.md)                | Konvertiert einen Videostream zwischen Farbformaten.       |
| [Frame Rate Konverter DSP](framerateconverter.md)       | Ändert die Framerate eines Videodaten Stroms.            |
| [Video Resizer DSP](videoresizer.md)                    | Ändert die Größe eines Videodaten Stroms.                              |
| [Sprach Erfassungs-DSP](voicecapturedmo.md)                 | Kapselt mehrere DSPs, die mit der sprach Erfassung verknüpft sind.  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmierreferenz](media-foundation-programming-reference.md)
</dt> </dl>

 

 
