---
title: Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen
description: Es gibt Richtlinien, die Sie beachten müssen, wenn Sie eine Zusammenfassungs Informations Eigenschaft für den strukturierten Speicher implementieren.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707301"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen

Es gibt Richtlinien, die Sie beachten müssen, wenn Sie eine Zusammenfassungs Informations Eigenschaft für den strukturierten Speicher implementieren.

Im folgenden sind die Richtlinien für die Implementierung [des Eigenschaften Satzes für Zusammenfassungs Informationen](the-summary-information-property-set.md)aufgeführt:

-   **PID \_ Die Vorlage** verweist auf ein externes Dokument, das Format-und Stil Informationen enthält. Der Prozess, mit dem sich die Vorlage befindet, ist Implementierungs definiert.
-   **PID \_ Lastauthor** ist der Name, der von der Anwendung in Benutzerinformationen gespeichert wird. Mary erstellt z. b. ein Dokument auf dem Computer und übergibt es John, das es dann ändert und speichert. Mary ist Autor, John ist der letzte gespeicherte Wert.
-   **PID \_ "Revnumber** " gibt an, wie oft der Datei-/Speicherbefehl für dieses Dokument aufgerufen wurde.
-   Alle Datums-/Uhrzeitwerte müssen in UTC (Universal koordinierte Time) gespeichert werden.
-   **PID \_ Create \_ DTM** ist eine schreibgeschützte Eigenschaft. Diese Eigenschaft sollte beim Erstellen eines Dokuments festgelegt werden, sollte jedoch nicht später geändert werden.
-   Für die **PID- \_ Miniaturansicht** sollten Anwendungen Daten im **CF- \_ DIB** -oder **CF- \_ MetafilePict** -Format speichern. **CF \_ MetafilePict** wird empfohlen.
-   **PID \_ Sicherheit** ist die empfohlene Sicherheitsstufe für das Dokument. Durch die Angabe der Sicherheitsstufe für das Dokument kann eine andere Anwendung als der Absender des Dokuments die Benutzeroberfläche an die Eigenschaften anpassen. In einer Anwendung sollten keine Informationen zu einem Kenn Wort geschützten Dokument angezeigt werden, oder es sollten keine Änderungen an den Erzwingung Read-Only oder auf Dokumente mit gesperrten Anmerkungen vorgenommen werden. Wenn der Benutzer versucht, Eigenschaften zu ändern, sollte die Anwendung den Benutzer über den Read-Only empfohlenen Status warnen.



| Sicherheitsstufe         | Wert |
|------------------------|-------|
| Keine                   | 0     |
| Kennwort geschützt     | 1     |
| Nur Lesen empfohlen  | 2     |
| Schreibgeschützt erzwungen     | 4     |
| Für Anmerkungen gesperrt | 8     |



 

 

 




