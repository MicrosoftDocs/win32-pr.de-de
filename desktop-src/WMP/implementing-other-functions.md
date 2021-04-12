---
title: Implementieren anderer Funktionen
description: Implementieren anderer Funktionen
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- Visualisierungen, iwmpeffects-Schnittstelle
- benutzerdefinierte Visualisierungen, iwmpeffects-Schnittstelle
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Funktion "Rendering", zusätzliche Funktionen
- Iwmpeffects-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed6efa5cc9a0697653e558f27165b66d5f230fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389892"
---
# <a name="implementing-other-functions"></a>Implementieren anderer Funktionen

Sie möchten eine eigene Implementierung der Funktion " **Rendering** " schreiben. Es werden mehrere weitere Funktionen bereitgestellt, die auch Element Funktionen der **iwmpeffects** -Schnittstelle sind. Einige erhalten zusätzliche Informationen, die Sie verwenden können, und andere stellen automatisch Windows Media Player mit vom Assistenten generierten Informationen bereit, wie z. b. den Namen der Visualisierung.

Die **iwmpeffects** -Schnittstelle unterstützt zusätzlich zum **Rendering** die folgenden Funktionen:



| Funktion                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Display PropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Die Standard Implementierung wird vom Assistenten nicht bereitgestellt.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Ruft die Funktionen der Visualisierung ab und übergibt sie an Windows Media Player.                                                                                                                                                                                                                     |
| [Getcurrentvoreinstellung](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | Der Assistent hat beim Generieren des Codes für die Visualisierung zwei Voreinstellungen erstellt. Diese Funktion wird aufgerufen, wenn der Skin-Entwickler den Index der aktuellen Voreinstellung erhalten möchte. Sie möchten die Implementierung dieser Funktion nicht ändern, da Sie lediglich von anderen Funktionen festgelegte Informationen verwendet. |
| [Getpresetcount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | Der Assistent hat beim Generieren des Codes für die Visualisierung zwei Voreinstellungen erstellt. Sie können die Anzahl ändern, indem Sie die Implementierung von **getpresetcount** ändern. Weitere Informationen zum Ändern der Voreinstellungen finden Sie unter [Voreinstellungen](presets.md) .                                                             |
| [Getpresettitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | Der Assistent hat beim Generieren des Codes für die Visualisierung zwei Voreinstellungen erstellt. Sie können die verwendeten Titel ändern, indem Sie die Implementierung von **getpresettitle** ändern. Weitere Informationen zum Ändern der Voreinstellungen finden Sie unter [Voreinstellungen](presets.md) .                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Ruft den Titel der Visualisierung ab und übergibt ihn an den Windows-Media Player. Der Assistent hat den Namen des Projekts verwendet, um den Namen zu generieren, der zurückgegeben wird.                                                                                                                                           |
| [Gofullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Die Standard Implementierung wird vom Assistenten nicht bereitgestellt.                                                                                                                                                                                                                                                           |
| [' MediaInfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Ruft die Anzahl der Audiokanäle und die Samplingrate der aktuell wiedergegebenen Audiodaten ab.                                                                                                                                                                                                               |
| [Renderfullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Die Standard Implementierung wird vom Assistenten nicht bereitgestellt.                                                                                                                                                                                                                                                           |
| [Setcurrentvoreinstellung](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | Der Assistent hat beim Generieren des Codes für die Visualisierung zwei Voreinstellungen erstellt. Diese Funktion wird aufgerufen, wenn Windows Media Player zu einer benannten Voreinstellung wechseln möchte.                                                                                                                                   |



 

Die **IWMPEffects2** -Schnittstelle unterstützt die folgenden zusätzlichen Funktionen:



| Funktion                                            | BESCHREIBUNG                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | Wenn Sie in einem Fenster rendern, ruft Windows Media Player diese Funktion auf, damit Sie ein neues Fenster zum Rendern erstellen können.                          |
| [Zerstören](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | Wenn Sie in einem Fenster rendern, ruft Windows Media Player diese Funktion auf, damit Sie das Fenster, das Sie beim Aufrufen von **Create** erstellt haben, zerstören können. |
| [Notifynewmedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Mit dieser Funktion kann ihre Visualisierung Antworten, wenn ein neues Medien Element vom Player geladen wurde.                                          |
| [Onwindowmessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Diese Funktion empfängt Windows-Meldungen vom Player, wenn Sie im fensterlosen Modus gerendert wird.                                                       |
| [Renderwindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Diese Funktion wird vom Player anstelle von **iwmpeffects:: Rendering** aufgerufen, wenn der Player im Fenstermodus gerendert wird.                          |
| [Setcore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Diese Funktion empfängt einen Zeiger auf die **iwmpcore** -Schnittstelle.                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren des Codes**](implementing-your-code.md)
</dt> </dl>

 

 




