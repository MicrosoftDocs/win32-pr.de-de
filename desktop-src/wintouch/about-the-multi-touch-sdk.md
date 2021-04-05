---
title: Info zur Windows-Eingabe
description: Dieses Thema enthält eine kurze Übersicht über Windows-Finger Eingaben.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows-Fingereingabe, Software Development Kit
- Windows-Touchscreen, SDK
- Windows-Kontakt, Info
- Windows-Fingereingabe, neue Features
- Windows-Fingereingabe, Neuerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e9a3ebab9a5c85127a1548c07c2ea0fa2cae54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947436"
---
# <a name="about-windows-touch"></a>Info zur Windows-Eingabe

Dieses Thema enthält eine kurze Übersicht über Windows-Finger Eingaben.

Neue Hardware-und API-Elemente im Windows 7-Betriebssystem bieten Anwendungen die Möglichkeit, Eingaben von mehreren Kontakten zu empfangen. Dies ermöglicht es solchen Anwendungen, mehrere gleichzeitige Berührungspunkte auf der sichtbaren Oberfläche der Anwendung zu erkennen und darauf zu reagieren. Die Funktionalität für dieses Feature in Windows 7 wird durch eine neue Meldung bereitgestellt, die von den Berichten und Nachverfolgen berührt wird. Die neue Nachricht, [**WM \_ berühren**](wm-touchdown.md), meldet die Aktion (nach oben, nach unten, Verschiebung), Position und einen Bezeichner für Berührungspunkte. Windows-Finger Eingabenachrichten werden von Windows generiert und an Windows übermittelt, die sich für Windows-Fingereingabe Eingaben registrieren.

Zusätzlich zur neuen toucheingabenachricht wurden der vorhandenen Liste der Fenster Meldungen Gesten Meldungen hinzugefügt. Die Messaging Unterstützung für Gesten wird durch eine einzelne neue Fenster Meldung ([**WM- \_ Geste**](wm-gesture.md)) aktiviert, die an entsprechende Anwendungsfenster gesendet oder an diese gesendet wird, wenn Benutzereingaben als Geste erkannt werden. Dedizierte API-Funktionen kapseln die Details für die Erstellung und den Verbrauch dieser Nachricht. Dies ist der Fall, da sich die der Nachricht zugeordneten Informationen in der Zukunft ändern können, ohne dass Anwendungen, die diese Nachricht bereits nutzen, unterbrochen werden.

Neben Gesten Nachrichten wurden dem Windows SDK spezialisierte Schnittstellen hinzugefügt. Diese Schnittstellen ermöglichen erweiterte Unterstützung für Berührungs Eingaben, damit Anwendungsentwickler problemlos natürliche Benutzeroberflächen erstellen können. Die [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) -Schnittstelle interpretiert WM-Fingereingabe Meldungen, um Ereignisse mit Übersetzungs-, Rotations-und Skalierungsinformationen über eine Auflistung von Berührungspunkten zu erhalten. [**\_**](wm-touchdown.md) Die [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) -Schnittstelle kann in Verbindung mit der **IManipulationProcessor** -Schnittstelle verwendet werden, um Animationen zu aktivieren und sicherzustellen, dass Objekte auf dem Bildschirm des Benutzers bleiben, wenn Sie verschoben werden.

API-Elemente für Windows-Finger Eingaben haben einige Ähnlichkeiten mit dem Microsoft Pixel Sense SDK (ehemals Microsoft Surface SDK), Anwendungen, die auf Microsoft Pixel Sense abzielen, werden jedoch nicht auf Windows-Touchscreen-Computern ausgeführt. Außerdem können Anwendungen, die auf Windows-Finger Eingaben abzielen, nicht unter Microsoft Pixel Sense ausgeführt werden.

Einige der Funktionen von Windows-Finger Eingaben sind in den Kern von Windows 7 integriert. Diese Funktion ist für Benutzer verfügbar, ohne dass Entwickler die Unterstützung explizit aktivieren müssen. Um Windows-Finger Eingaben in vollem Umfang nutzen zu können, müssen Entwickler jedoch die Windows-Eingabe-API verwenden. Informationen zu den ersten Schritten mit der Funktionsweise von Windows Touchscreen finden Sie im [Programmier Handbuch](programming-guide.md) , oder beginnen Sie mit [der Auswahl des richtigen Ansatzes für Windows](choosing-the-right-approach-to-windows-touch.md)-Finger Eingaben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Architektur](architectural-overview.md)
</dt> <dt>

[Auswählen des richtigen Ansatzes für Windows-Finger Eingaben](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows-Fingereingabe](windows-touch-portal.md)
</dt> </dl>

 

 




