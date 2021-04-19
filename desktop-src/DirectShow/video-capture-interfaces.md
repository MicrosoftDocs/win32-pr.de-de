---
description: Video Erfassungs Schnittstellen
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Video Erfassungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356572"
---
# <a name="video-capture-interfaces"></a>Video Erfassungs Schnittstellen

Diese Schnittstellen unterstützen die Video Erfassung mithilfe von Microsoft® Windows® Driver Model (WDM)-Geräten oder Legacy-Microsoft® Video für Windows® (Vfw)-Geräte.



| Schnittstelle                                                        | BESCHREIBUNG                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Iamanalog gvideodecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Steuern der Video Digitalisierung auf einer WDM-Video Erfassungs Karte.                                                      |
| [**Iambufferaushandlung**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Steuern Sie, wie eine PIN Puffer ordnet.                                                                         |
| [**Iamcopycapturefileprogress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Rückruf Schnittstelle zum Empfangen des Fortschritts eines Datei Kopiervorgangs.                                         |
| [**Iamcrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Erstellen Sie eine Hardware Verbindung zwischen einer WDM-Audiodatei oder Videoquelle und einem WDM-Erfassungsgerät.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Abfragen eines Erfassungs Filters zur Erfassung der Leistung.                                                            |
| [**Iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Steuern Sie die Start-und Endzeit der einzelnen Streams.                                                      |
| [**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Das Ausgabeformat des Erfassungs Filters wird abgefragt und festgelegt.                                                            |
| [**Iamvfwcapturedialogfelder**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Anzeigen der von VFW-Erfassungs Treibern bereitgestellten Dialogfelder.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Steuern Sie das Bild von einem Erfassungsgerät.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Passen Sie die Qualitäten eines Videosignals an, z. b. Helligkeit, Kontrast, Farbton, Sättigung, Gamma und Schärfe. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Buildfilterdiagramme für die Video Erfassung.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Geben Sie den Namen und die Attribute einer Ausgabedatei an.                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Externe Geräte Steuerungs Schnittstellen](external-device-control-interfaces.md)
</dt> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



