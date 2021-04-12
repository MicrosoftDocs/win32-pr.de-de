---
description: Eine zyklische Redundanz Überprüfung (CRC) von Dateien ist mit Windows Installer verfügbar.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: CRC-Überprüfung während einer Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217178"
---
# <a name="crc-checking-during-an-installation"></a>CRC-Überprüfung während einer Installation

Eine zyklische Redundanz Überprüfung (CRC) von Dateien ist mit Windows Installer verfügbar. Die CRC-Überprüfung ist ein Fehler Überprüfungsverfahren, ähnlich wie eine Prüfsumme, mit dem eine Anwendung ermitteln kann, ob die Informationen in einer Datei geändert wurden. Nachdem die Windows Installer das Kopieren einer Datei abgeschlossen hat, ruft Sie einen CRC-Wert aus den Quell-und Zieldateien ab. Das Installationsprogramm überprüft den ursprünglichen CRC-Stempel in die Datei und vergleicht diesen mit dem CRC, der aus der Kopie berechnet wurde. Die CRC-Überprüfung schlägt fehl, wenn der ursprüngliche CRC-Wert ungleich NULL ist und sich von dem CRC unterscheidet, der für den Kopiervorgang berechnet wurde. Wenn das ursprüngliche CRC NULL ist, erfolgt keine Überprüfung.

Der Windows Installer führt in den folgenden Fällen eine CRC-Prüfung für eine Datei durch:

-   Wenn die [msicheckcrcs-Eigenschaft](msicheckcrcs.md) festgelegt ist und **msidbFileAttributesChecksum** im Feld Attribute des Datensatzes der Datei in der [Dateitabelle](file-table.md)enthalten ist. Das Installationsprogramm führt die CRC-Prüfung einmal nach dem installieren, duplizieren oder Verschieben der Datei durch.
-   Wenn die [Eigenschaft msicheckcrcs](msicheckcrcs.md) festgelegt ist und **msidbFileAttributesChecksum** im Feld Attribute des Datensatzes der Datei in der [Dateitabelle](file-table.md)enthalten ist, führt das Installationsprogramm nach dem Patchen der Datei eine CRC-Prüfung durch.
-   Wenn **msidbFileAttributesChecksum** im Feld Attribute des Datensatzes der Datei in der [Dateitabelle](file-table.md)enthalten ist, führt das Installationsprogramm eine CRC-Überprüfung vor dem Binden von Images durch.

Wenn die Überprüfung fehlschlägt, bevor ein Abbild gebunden wird, meldet das Installationsprogramm die folgenden beiden Fehler in der Protokolldatei und setzt die Installation fort, ohne die Datei zu binden.



| Code | `Message`                                               |
|------|-------------------------------------------------------|
| 2941 | CRC für Datei 2 kann nicht berechnet werden \[ \] .             |
| 2942 | Die BindImage-Aktion wurde für \[ zwei Dateien nicht ausgeführt \] . |



 

Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei kopiert, dupliziert oder gepatcht wurde, meldet das Installationsprogramm den folgenden Fehler. Dieser Fehler wird auch gemeldet, wenn die Überprüfung fehlschlägt, nachdem eine komprimierte Datei kopiert wurde. Wenn die Datei über das **msidbfileattributesvital** -Attribut verfügt, wird die Datei als wichtig für die Installation angesehen, und der Benutzer erhält die Möglichkeit, die Installation zu wiederholen oder abzubrechen. Wenn die Datei in der Spalte Attribute der [Dateitabelle](file-table.md)als nicht entscheidend gekennzeichnet ist, kann der Benutzer den Fehler ignorieren und den Vorgang fortsetzen, den Vorgang wiederholen oder die Installation abbrechen.



| Code | `Message`                                         |
|------|-------------------------------------------------|
| 1331 | Fehler beim Kopieren von \[ 2 \] Datei: CRC-Fehler. |



 

Beachten Sie, dass nur nicht komprimierte Dateien verschoben werden. Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei verschoben wurde, zeigt das Installationsprogramm den folgenden Fehler an. Wenn die Datei über das **msidbfileattributesvital** -Attribut verfügt, wird die Datei als wichtig für die Installation angesehen, und die Installation schlägt fehl. Wenn die Datei in der Spalte Attribute der [Dateitabelle](file-table.md)als nicht entscheidend gekennzeichnet ist, erhält der Benutzer die Option, den Fehler abzubrechen oder zu ignorieren und die Installation fortzusetzen.



| Code | `Message`                                         |
|------|-------------------------------------------------|
| 1332 | Fehler beim Verschieben von \[ 2 \] Datei: CRC-Fehler. |



 

Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei gepatcht wurde, zeigt das Installationsprogramm den folgenden Fehler an. Wenn die Datei über das **msidbfileattributesvital** -Attribut verfügt, wird die Datei als wichtig für die Installation angesehen, und die Installation schlägt fehl. Wenn die Datei in der Spalte Attribute der [Dateitabelle](file-table.md)als nicht entscheidend gekennzeichnet ist, erhält der Benutzer die Option, den Fehler abzubrechen oder zu ignorieren und die Installation fortzusetzen.



| Code | `Message`                                          |
|------|--------------------------------------------------|
| 1333 | Fehler beim Patchen der \[ 2- \] Datei: CRC-Fehler. |



 

 

 



