---
description: Videoaufnahmeschnittstellen
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Videoaufnahmeschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfee9807a94f381fef3a294dcd405de6fe8b67fafef3ace562309fe5e10d2ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633060"
---
# <a name="video-capture-interfaces"></a>Videoaufnahmeschnittstellen

Diese Schnittstellen unterstützen die Videoerfassung mithilfe von WDM-Geräten (Microsoft® Windows® Driver Model) oder älteren Microsoft® Video for Windows®(VFW)-Geräten.



| Schnittstelle                                                        | BESCHREIBUNG                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Steuern der Videodigitalisierung auf einer WDM-Videoaufnahmekarte                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Steuert, wie ein Stecknadel Puffer zuordnet.                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Rückrufschnittstelle zum Empfangen des Status eines Dateikopiervorgangs.                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Erstellen Sie eine Hardwareverbindung zwischen einer WDM-Audio- oder Videoquelle und einem WDM-Erfassungsgerät.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Fragen Sie einen Erfassungsfilter zur Erfassungsleistung ab.                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Steuern Sie die Start- und Beendigungszeiten einzelner Streams.                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Fragen Sie das Ausgabeformat des Erfassungsfilters ab, und legen Sie es fest.                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Zeigt die dialogfelder an, die von VFW-Erfassungstreibern bereitgestellt werden.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Steuern Sie das Bild von einem Erfassungsgerät aus.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Passen Sie die Qualitäten eines Videosignals wie Helligkeit, Kontrast, Farbton, Sättigung, Gamma und Schärfe an. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Erstellen sie Filterdiagramme für die Videoaufnahme.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Geben Sie den Namen und die Attribute einer Ausgabedatei an.                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Externe Gerätesteuerungsschnittstellen](external-device-control-interfaces.md)
</dt> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



