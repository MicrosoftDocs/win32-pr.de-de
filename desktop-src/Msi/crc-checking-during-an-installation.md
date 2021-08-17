---
description: Eine zyklische Redundanzprüfung (CRC) von Dateien ist mit dem Windows verfügbar.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: CRC-Überprüfung während einer Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b80a9b1900abf6c294911803df155a4c75025f5ad5ef01609af7345b0431e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379915"
---
# <a name="crc-checking-during-an-installation"></a>CRC-Überprüfung während einer Installation

Eine zyklische Redundanzprüfung (CRC) von Dateien ist mit dem Windows verfügbar. Die CRC-Überprüfung ist ein Fehlerüberprüfungsmechanismus, der einer Prüfsumme ähnelt und es einer Anwendung ermöglicht, zu bestimmen, ob die Informationen in einer Datei geändert wurden. Nachdem der Windows Installer das Kopieren einer Datei abgeschlossen hat, ruft er einen CRC-Wert sowohl aus der Quell- als auch aus der Zieldatei ab. Das Installationsprogramm überprüft die ursprüngliche CRC, die in die Datei gestempelt ist, und vergleicht diese mit der CRC, die aus der Kopie berechnet wurde. Die CRC-Überprüfung schlägt fehl, wenn der ursprüngliche CRC-Wert nicht NULL ist und sich von der für die Kopie berechneten CRC-Datei abt. Wenn die ursprüngliche CRC NULL ist, erfolgt keine Überprüfung.

Der Windows Installer führt in den folgenden Fällen eine CRC-Überprüfung für eine Datei durch:

-   Wenn die [MSICHECKCRCS-Eigenschaft](msicheckcrcs.md) festgelegt ist und **msidbFileAttributesChecksum** im Feld Attribute des Dateidateneintrags in der [Dateitabelle enthalten ist.](file-table.md) Das Installationsprogramm führt die CRC-Überprüfung einmal durch, nachdem die Datei installiert, dupliziert oder bewegt wurde.
-   Wenn die [MSICHECKCRCS-Eigenschaft](msicheckcrcs.md) festgelegt ist und **msidbFileAttributesChecksum** im Feld Attribute des Dateidateneintrags in der [Dateitabelle](file-table.md)enthalten ist, führt das Installationsprogramm nach dem Patchen der Datei eine CRC-Überprüfung durch.
-   Wenn **msidbFileAttributesChecksum** im Feld Attribute des Dateidateneintrags in der Tabelle Datei enthalten [ist,](file-table.md)führt das Installationsprogramm eine CRC-Überprüfung durch, bevor Images bindungsbasiert werden.

Wenn die Überprüfung vor dem Binden eines Images fehlschlägt, meldet das Installationsprogramm die folgenden beiden Fehler in der Protokolldatei und setzt die Installation fort, ohne die Datei zu binden.



| Code | `Message`                                               |
|------|-------------------------------------------------------|
| 2941 | Die CRC für Datei 2 kann nicht \[ berechnet \] werden.             |
| 2942 | Die BindImage-Aktion wurde für \[ 2 Dateien nicht \] ausgeführt. |



 

Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei kopiert, dupliziert oder gepatcht wurde, meldet das Installationsprogramm den folgenden Fehler. Dieser Fehler wird auch gemeldet, wenn die Überprüfung nach dem Kopieren einer komprimierten Datei fehlschlägt. Wenn die Datei über das **Attribut msidbFileAttributesVital** verfügt, wird die Datei als wichtig für die Installation angesehen, und der Benutzer erhält die Option, die Installation erneut zu versuchen oder abzubricht. Wenn die Datei in der Spalte Attribute der Tabelle Datei als nicht benutzerfreundlich markiert [ist,](file-table.md)kann der Benutzer den Fehler ignorieren und die Installation fortsetzen, wiederholen oder abbrechen.



| Code | `Message`                                         |
|------|-------------------------------------------------|
| 1331 | Fehler beim ordnungsgemäßen Kopieren \[ der \] 2-Datei: CRC-Fehler. |



 

Beachten Sie, dass nur unkomprimierte Dateien verschoben werden. Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei verschoben wurde, zeigt das Installationsprogramm den folgenden Fehler an. Wenn die Datei über das **Attribut msidbFileAttributesVital** verfügt, wird die Datei als wichtig für die Installation betrachtet, und die Installation schlägt fehl. Wenn die Datei in der Spalte Attribute der Tabelle Datei als nicht benutzerfreundlich markiert [ist,](file-table.md)erhält der Benutzer die Möglichkeit, den Fehler abzubricht oder zu ignorieren und die Installation fortzufahren.



| Code | `Message`                                         |
|------|-------------------------------------------------|
| 1332 | Fehler beim ordnungsgemäßen Verschieben \[ der \] 2-Datei: CRC-Fehler. |



 

Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei gepatcht wurde, zeigt das Installationsprogramm den folgenden Fehler an. Wenn die Datei über das **Attribut msidbFileAttributesVital** verfügt, wird die Datei als wichtig für die Installation betrachtet, und die Installation schlägt fehl. Wenn die Datei in der Spalte Attribute der Tabelle Datei als nicht benutzerfreundlich markiert [ist,](file-table.md)erhält der Benutzer die Möglichkeit, den Fehler abzubricht oder zu ignorieren und die Installation fortzufahren.



| Code | `Message`                                          |
|------|--------------------------------------------------|
| 1333 | Fehler beim ordnungsgemäßen \[ Patchen der \] 2-Datei: CRC-Fehler. |



 

 

 



