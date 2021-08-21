---
title: Implementieren anderer Funktionen
description: Implementieren anderer Funktionen
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- Visualisierungen,IWMPEffects-Schnittstelle
- Benutzerdefinierte Visualisierungen, IWMPEffects-Schnittstelle
- Visualisierungen,Render-Funktion
- Benutzerdefinierte Visualisierungen, Renderfunktion
- Renderfunktion,zusätzliche Funktionen
- IWMPEffects-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73392204357ec856c5c04f2a0f24028ea29e5f09c3aa203d95ed8e2cc7e4ded3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508930"
---
# <a name="implementing-other-functions"></a>Implementieren anderer Funktionen

Sie sollten auf jeden Fall Ihre eigene Implementierung der **Render-Funktion** schreiben. Es werden mehrere weitere Funktionen bereitgestellt, die auch Memberfunktionen der **IWMPEffects-Schnittstelle** sind. Einige stellen Ihnen zusätzliche Informationen zur Verfügung, die Sie verwenden können, während andere Windows Media Player automatisch Informationen bereitstellen, die vom Assistenten generiert wurden, z. B. den Namen Ihrer Visualisierung.

Die **IWMPEffects-Schnittstelle** unterstützt zusätzlich zum Rendern die folgenden **Funktionen:**



| Funktion                                                   | Beschreibung                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Die Standardimplementierung wird vom Assistenten nicht bereitgestellt.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Ruft die Funktionen Ihrer Visualisierung ab und übergibt sie Windows Media Player.                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | Der Assistent hat zwei Voreinstellungen erstellt, als er den Code für Ihre Visualisierung generiert hat. Diese Funktion wird aufgerufen, wenn der Skinentwickler den Index der aktuellen Voreinstellung erhalten möchte. Sie möchten die Implementierung dieser Funktion nicht ändern, da sie nur informationen verwendet, die von anderen Funktionen festgelegt wurden. |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | Der Assistent hat zwei Voreinstellungen erstellt, als er den Code für Ihre Visualisierung generiert hat. Sie können die Anzahl ändern, indem Sie die Implementierung von **GetPresetCount ändern.** Weitere [Informationen zum Ändern](presets.md) der Voreinstellungen finden Sie unter Voreinstellungen.                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | Der Assistent hat zwei Voreinstellungen erstellt, als er den Code für Ihre Visualisierung generiert hat. Sie können die verwendeten Titel ändern, indem Sie die Implementierung von **GetPresetTitle ändern.** Weitere [Informationen zum Ändern](presets.md) der Voreinstellungen finden Sie unter Voreinstellungen.                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Ruft den Titel Ihrer Visualisierung ab und übergibt ihn Windows Media Player. Der Assistent hat den Namen Ihres Projekts verwendet, um den Namen zu generieren, der zurücküberkommen wird.                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Die Standardimplementierung wird vom Assistenten nicht bereitgestellt.                                                                                                                                                                                                                                                           |
| [Mediainfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Ruft die Anzahl der Audiokanäle und die Abtastrate der aktuell abspielten Audiodaten ab.                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Die Standardimplementierung wird vom Assistenten nicht bereitgestellt.                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | Der Assistent hat zwei Voreinstellungen erstellt, als er den Code für Ihre Visualisierung generiert hat. Diese Funktion wird aufgerufen, wenn Windows Media Player in eine benannte Voreinstellung ändern möchte.                                                                                                                                   |



 

Die **IWMPEffects2-Schnittstelle** unterstützt die folgenden zusätzlichen Funktionen:



| Funktion                                            | BESCHREIBUNG                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erstellen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | Beim Rendern in einem Fenster ruft Windows Media Player funktion auf, damit Sie ein neues Fenster für das Rendering erstellen können.                          |
| [Zerstören](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | Beim Rendern in einem Fenster ruft Windows Media Player Funktion auf, damit Sie das Fenster zerstören können, das Sie beim Aufrufen von **Create** erstellt haben. |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Mit dieser Funktion kann Ihre Visualisierung reagieren, wenn ein neues Medienelement vom Player geladen wurde.                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Diese Funktion empfängt Windows-Nachrichten vom Player, wenn sie im fensterlosen Modus gerendert wird.                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Diese Funktion wird vom Player anstelle von **IWMPEffects::Render** aufgerufen, wenn der Player im Fenstermodus gerendert wird.                          |
| [SetCore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Diese Funktion empfängt einen Zeiger auf die **IWMPCore-Schnittstelle.**                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren ihres Codes**](implementing-your-code.md)
</dt> </dl>

 

 




