---
description: Ab Windows XP unterstützt Systemsteuerung die Kategorisierung von Systemsteuerung Elementen. Elemente werden so registriert, dass sie in einer oder mehreren Kategorien angezeigt werden. Neue Kategorien können nicht erstellt werden.
title: Zuweisen Systemsteuerung Kategorien
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b6785a786bfe80f5a5b13bc5e9dfbe39507a2c9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478486"
---
# <a name="assigning-control-panel-categories"></a>Zuweisen Systemsteuerung Kategorien

Ab Windows XP unterstützt Systemsteuerung die Kategorisierung von Systemsteuerung Elementen. Elemente werden so registriert, dass sie in einer oder mehreren Kategorien angezeigt werden. Neue Kategorien können nicht erstellt werden.

Um ein Systemsteuerung Element in einer oder mehreren Kategorien zu registrieren, fügen Sie werte hinzu, wie im Abschnitt [Executable Systemsteuerung Item Registration](registering-control-panel-items.md) oder DLL Systemsteuerung Item [Registration](registering-control-panel-items.md) von [Registering Systemsteuerung Items](registering-control-panel-items.md)beschrieben.




| Kategorie-ID | Kategoriename (Windows 7) | Kategoriename (Windows Vista) | Kategoriename (Windows XP) | 
|-------------|---------------------------|-------------------------------|----------------------------|
| 0 | "Alle Systemsteuerung Elemente" | "Zusätzliche Optionen"<blockquote>[!Note]<br />Jedes Systemsteuerung Element, das keine Kategorie-ID angibt, wird in dieser Kategorie angezeigt.</blockquote><br /> | "Andere Systemsteuerung Optionen"<blockquote>[!Note]<br />Jedes Systemsteuerung Element, das keine Kategorie-ID angibt, wird in dieser Kategorie angezeigt.</blockquote><br /> | 
| 1 | "Darstellung und Personalisierung" | "Darstellung und Personalisierung" | "Darstellung und Designs" | 
| 2 | "Hardware und Sound" | "Hardware und Sound" | "Drucker und andere Hardware" | 
| 3 | "Netzwerk und Internet" | "Netzwerk und Internet" | "Netzwerk- und Internetverbindungen" | 
| 4 | Nicht mehr verwendet. Jedes Element, das sich nur zu Kategorie 4 hinzufügt, wird in Kategorie 2 (Hardware und Sound) angezeigt. | Nicht mehr verwendet. Jedes Element, das sich nur zu Kategorie 4 hinzufügt, wird in Kategorie 2 (Hardware und Sound) angezeigt. | "Sounds, Speech und Audiogeräte" | 
| 5 | "System und Sicherheit" | "System und Wartung" | "Leistung und Wartung" | 
| 6 | "Uhr, Sprache und Region" | "Uhr, Sprache und Region" | "Datum, Uhrzeit, Sprache und regionale Optionen" | 
| 7 | "Erleichterte Bedienung" | "Erleichterte Bedienung" | "Barrierefreiheitsoptionen" | 
| 8 | "Programme" | "Programme" | "Programme hinzufügen oder entfernen" | 
| 9 | "Benutzerkonten"<blockquote>[!Note]<br />Wenn keine Verbindung mit einer Domäne besteht, wird dies als "Benutzerkonten und Family Safety" bezeichnet.</blockquote><br /> | "Benutzerkonten"<blockquote>[!Note]<br />Wenn keine Verbindung mit einer Domäne besteht, wird dies als "Benutzerkonten und Family Safety" bezeichnet.</blockquote><br /> | "Benutzerkonten" | 
| 10 | Nicht mehr verwendet. In dieser Kategorie registrierte Elemente werden in Kategorie 5 (System und Sicherheit) angezeigt. | "Security" | "Security Center"<blockquote>[!Note]<br />Nur in Windows XP Service Pack 2 (SP2) oder höher verfügbar.</blockquote><br /> | 
| 11 | Nicht mehr verwendet. In dieser Kategorie registrierte Elemente werden in Kategorie 0 (Alle Systemsteuerung Elemente) angezeigt. | "Mobiler PC"<blockquote>[!Note]<br />Diese Kategorie ist nur auf mobilen PCs sichtbar.</blockquote><br /> | Nicht verwendet. | 




 

In Windows XP unterscheiden sich die Kategorien Software und **Benutzerkonten** hinzufügen **oder entfernen** von anderen Kategorien in Systemsteuerung. Wenn mindestens ein Element einer dieser beiden Kategorien hinzugefügt wird, öffnet der zugeordnete Link in Systemsteuerung eine Kategorieseite. Die registrierten Elemente werden im unteren Teil der Seite unter der Überschrift "oder Pick a Systemsteuerung icon" angezeigt. Wenn keine Elemente für eine dieser Kategorien registriert sind, ruft der zugeordnete Link in Systemsteuerung den Standard-Windows Element für diese Kategorie direkt auf. In Windows Vista und höher verfügen die Kategorie **Programme** und die Kategorie **Benutzerkonten** nicht über diese Eigenschaft.

Die **kategorie Security Center,** die nur in Windows XP SP2 verfügbar ist, ist ebenfalls nicht standardmäßig. Wenn Sie auf diese Kategorie klicken, wird die **seite Security Center** in einem neuen Fenster geöffnet. Elemente, die für **Security Center** registriert sind, werden im unteren Teil dieser Seite unter der Überschrift **Sicherheitseinstellungen verwalten für angezeigt:**. Durch Klicken auf ein Symbol wird das Systemsteuerung Element geöffnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Items](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[Registrieren von Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPLApplet](using-cplapplet.md)
</dt> <dt>

[Systemsteuerung Nachrichtenverarbeitung](message-processing.md)
</dt> <dt>

[Ausführen von Systemsteuerung Elementen](executing-control-panel-items.md)
</dt> <dt>

[Erweitern von System Systemsteuerung Elementen](extending-system-control-panel-items.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für ein Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




