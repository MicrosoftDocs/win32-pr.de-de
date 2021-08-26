---
title: Informationen zu Windows Touch
description: Dieses Thema bietet eine kurze Übersicht über Windows Touch.
ms.assetid: 19100652-3778-4f25-8d54-70e70363239b
keywords:
- Windows Touch, Software Development Kit
- Windows Toucheingabe, SDK
- Windows Toucheingabe, Informationen
- Windows Toucheingabe, neue Features
- Windows Toucheingabe, Neuerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3d86270ea6c43cc37c39a5d29282a0451dd38d312b996041dcd21f30de8d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881531"
---
# <a name="about-windows-touch"></a>Informationen zu Windows Touch

Dieses Thema bietet eine kurze Übersicht über Windows Touch.

Neue Hardware- und API-Elemente im betriebssystem Windows 7 bieten Anwendungen die Möglichkeit, Eingaben von mehreren Kontakten zu empfangen. Dadurch können solche Anwendungen mehrere gleichzeitige Berührungspunkte auf der sichtbaren Oberfläche der Anwendung erkennen und darauf reagieren. Die Funktionalität für dieses Feature in Windows 7 wird durch eine neue Meldung bereitgestellt, die Berührungen meldet und nachzeichnet. Die neue Meldung [**WM \_ TOUCH**](wm-touchdown.md)meldet die Aktion (nach oben, unten, verschieben), position und einen Bezeichner für Berührungspunkte. Windows Touchnachrichten werden von Windows generiert und an Fenster übermittelt, die sich für Windows Toucheingabe registrieren.

Zusätzlich zur neuen Toucheingabenachricht wurden der vorhandenen Liste der Fenstermeldungen Gestennachrichten hinzugefügt. Die Messagingunterstützung für Gesten wird durch eine einzelne neue Fenstermeldung [**(WM \_ GESTURE)**](wm-gesture.md)aktiviert, die gesendet oder an entsprechende Anwendungsfenster gesendet wird, wenn Benutzereingaben als Geste erkannt werden. Dedizierte API-Funktionen kapseln die Details für die Erstellung und Nutzung dieser Nachricht. Dies geschieht, da sich die der Nachricht zugeordneten Informationen in Zukunft ändern können, ohne dass Anwendungen, die diese Nachricht bereits nutzen, nicht mehr stören.

Zusätzlich zu Gestennachrichten wurden dem Windows SDK spezielle Schnittstellen hinzugefügt. Diese Schnittstellen ermöglichen erweiterte Unterstützung für Toucheingaben, sodass Anwendungsentwickler ganz einfach natürliche Benutzeroberflächen erstellen können. Die [**IManipulationProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interpretiert [**WM \_ TOUCH-Nachrichten,**](wm-touchdown.md) um Ereignisse auszublenden, die Übersetzungs-, Drehungs- und Skalierungsinformationen zu einer Sammlung von Berührungspunkten enthalten. Die [**IInertiaProcessor-Schnittstelle**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) kann in Verbindung mit der **IManipulationProcessor-Schnittstelle** verwendet werden, um Animationen zu ermöglichen und sicherzustellen, dass Objekte beim Verschieben auf dem Bildschirm des Benutzers verbleiben.

API-Elemente für Windows Touch weisen einige Ähnlichkeiten mit dem Microsoft PixelSense SDK (früher als Microsoft Surface SDK bezeichnet) auf, aber Anwendungen für Microsoft PixelSense werden nicht auf Windows Touch-Computern ausgeführt. Außerdem werden Anwendungen für Windows Touch nicht auf Microsoft PixelSense ausgeführt.

Ein Teil der Funktionalität von Windows Touch ist in den Kern von Windows 7 integriert. Diese Funktionalität ist für Benutzer verfügbar, ohne dass Entwickler die Unterstützung explizit aktivieren müssen. Um jedoch Windows Touch voll nutzen zu können, müssen Entwickler die Windows Touch-API verwenden. Informationen zur Funktionsweise von Windows Touch finden Sie im [Programmierhandbuch,](programming-guide.md) oder beginnen Sie mit [Auswählen des richtigen Ansatzes zum Windows Touch.](choosing-the-right-approach-to-windows-touch.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Architektur](architectural-overview.md)
</dt> <dt>

[Auswählen des richtigen Ansatzes für die Windows Toucheingabe](choosing-the-right-approach-to-windows-touch.md)
</dt> <dt>

[Windows Touch](windows-touch-portal.md)
</dt> </dl>

 

 




