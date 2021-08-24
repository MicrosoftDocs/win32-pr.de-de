---
title: Implementieren des Eigenschaftensatzes für Zusammenfassungsinformationen
description: Beim Implementieren eines Zusammenfassungsinformationseigenschaftensatzes für strukturierte Storage müssen Richtlinien befolgt werden.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementieren des Eigenschaftensatzes für Zusammenfassungsinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe847d9a7353074727c94250d0f1ec1fec2194b5b7d250099464a86667861f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796910"
---
# <a name="implementing-the-summary-information-property-set"></a>Implementieren des Eigenschaftensatzes für Zusammenfassungsinformationen

Beim Implementieren eines Zusammenfassungsinformationseigenschaftensatzes für strukturierte Storage müssen Richtlinien befolgt werden.

Im Folgenden sind die Richtlinien für die Implementierung des [Eigenschaftensatzes für Zusammenfassungsinformationen aufgeführt:](the-summary-information-property-set.md)

-   **PID \_ TEMPLATE** bezieht sich auf ein externes Dokument, das Format- und Formatinformationen enthält. Der Prozess, in dem sich die Vorlage befindet, ist implementierungsdefiniert.
-   **PID \_ LASTAUTHOR** ist der Name, der von der Anwendung in Benutzerinformationen gespeichert wird. Mary erstellt beispielsweise ein Dokument auf ihrem Computer und übergibt es John, der es dann ändert und speichert. Mary ist die Autorin, John ist die letzte, die als Wert gespeichert wurde.
-   **PID \_ REVNUMBER** ist die Anzahl, mit der der Befehl Datei/Speichern für dieses Dokument aufgerufen wurde.
-   Jeder der Datums-/Uhrzeitwerte muss in der koordinierten Weltzeit (UTC) gespeichert werden.
-   **PID \_ CREATE \_ MF** ist eine schreibgeschützte Eigenschaft. Diese Eigenschaft sollte festgelegt werden, wenn ein Dokument erstellt wird, aber nicht später geändert werden.
-   Für **PID \_ THUMBNAIL** sollten Anwendungen Daten im **CF \_ DIB-** oder **CF \_ METAFILEPICT-Format** speichern. **CF \_ METAFILEPICT** wird empfohlen.
-   **PID \_ SICHERHEIT** ist die empfohlene Sicherheitsstufe für das Dokument. Durch Notieren der Sicherheitsstufe für das Dokument kann eine andere Anwendung als der Absender des Dokuments seine Benutzeroberfläche an die Eigenschaften anpassen. Eine Anwendung sollte keine Informationen zu einem kennwortgeschützten Dokument anzeigen oder Änderungen an erzwungenen Read-Only- oder Locked-for-Annotations-Dokumenten aktivieren. Wenn der Benutzer versucht, Eigenschaften zu ändern, sollte die Anwendung den Benutzer über den Read-Only Empfohlenen Status warnen.



| Sicherheitsstufe         | Wert |
|------------------------|-------|
| Keine                   | 0     |
| Kennwortgeschützt     | 1     |
| Schreibgeschützt empfohlen  | 2     |
| Schreibgeschützt erzwungen     | 4     |
| Gesperrt für Anmerkungen | 8     |



 

 

 




