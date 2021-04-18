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
# <a name="audio-capture-and-rendering-interfaces"></a>Schnittstellen für Audioerfassung und-Rendering

Diese Schnittstellen unterstützen Audioerfassung und Rendering in DirectShow.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Greifen Sie auf die analogen Eingaben auf der Soundkarte des Systems zu, und passen Sie die Merkmale an, wie z. b. Mono oder Stereo, Mischungs Ebene, Schwenk Pegel, Lautstärke, Treble und Bass. |
| [**Iamaudiorendererstats**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Erhalten Sie statistische Leistungsinformationen über das audiorendering.                                                                                          |
| [**Iambufferaushandlung**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Steuern Sie, wie der audioerfassungs Filter Puffer ordnet.                                                                                                   |
| [**Iamclockslave**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Steuern der Toleranz eines audiorenderers, wenn er mit einer anderen Uhr übereinstimmt.                                                                      |
| [**Iamdirectsound**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Ermöglicht es einer Anwendung, anzugeben, welches Fenster den Fokus hat, um die DirectSound-Audiowiedergabe zu steuern.                                                      |
| [**Iamresourcecontrol**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Speichern Sie eine Ressource für Audiogeräte, bevor Sie benötigt wird.                                                                                                        |
| [**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Das Ausgabeformat des Erfassungs Filters wird abgefragt und festgelegt.                                                                                                         |
| [**Ibasicaudiodatei**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Legen Sie audioausgabevolume und Saldo fest.                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen](interfaces.md)
</dt> </dl>

 

 



