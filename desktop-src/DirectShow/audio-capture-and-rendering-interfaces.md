---
description: Audioaufnahme- und Renderingschnittstellen
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Audioaufnahme- und Renderingschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ffdf586ec8566abddadcb0b7109680664963a63071472a3ac7aa895981e643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824250"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Audioaufnahme- und Renderingschnittstellen

Diese Schnittstellen unterstützen audio capture and rendering in DirectShow (Audioerfassung und -rendering in DirectShow).



| Schnittstelle                                              | Beschreibung                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Greifen Sie auf die analogen Eingaben auf der Soundkarte des Systems zu, und passen Sie Merkmale wie Mono oder Stereo, Mischungsebene, Schwenkebene, Lautheit, Treble und Lautheit an. |
| [**IAMAudioRendererStats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Hier finden Sie statistische Leistungsinformationen zum Audiorenderering.                                                                                          |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Steuern Sie, wie der Audioerfassungsfilter Puffer zuteilen soll.                                                                                                   |
| [**IAMClockSklave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Steuern Sie die Toleranz eines Audiorenderers, wenn er Raten mit einer anderen Uhr ab übereinstimmung.                                                                      |
| [**IAMDirectSound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Ermöglicht einer Anwendung anzugeben, welches Fenster den Fokus zum Steuern der DirectSound-Audiowiedergabe hat.                                                      |
| [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Speichern Sie eine Audiogeräteressource, bevor sie benötigt wird.                                                                                                        |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Fragen Sie das Ausgabeformat des Erfassungsfilters ab, und legen Sie es fest.                                                                                                         |
| [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Festlegen des Audioausgabevolumens und -ausgleichs.                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](interfaces.md)
</dt> </dl>

 

 



