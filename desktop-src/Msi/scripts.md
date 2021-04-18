---
description: Eine benutzerdefinierte Aktion kann Funktionen aufzurufen, die in VBScript oder JScript geschrieben sind.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358462"
---
# <a name="scripts"></a>Skripts

Eine benutzerdefinierte Aktion kann Funktionen aufzurufen, die in VBScript oder JScript geschrieben sind. Windows Installer stellt die Skript-Engine nicht bereit. Autoren, die während der Installation eine Skriptsprache verwenden möchten, müssen daher sicherstellen, dass die entsprechende Skript-Engine verfügbar ist.

Die JScript-Version 1,0 wird vom Installationsprogramm nicht unterstützt.

Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss explizit als 64 eine benutzerdefinierte 32-Bit-Aktion gekennzeichnet werden, indem das **msidbCustomActionType64BitScript** -Bit dem numerischen Typ benutzerdefinierte Aktionen in der Type-Spalte der [CustomAction](customaction-table.md) -Tabelle hinzugefügt wird. Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).

Die folgenden grundlegenden benutzerdefinierten Aktions Typen werden in Skripts geschriebene Funktionen aufgerufen.



| Benutzerdefinierter Aktionstyp                                 | BESCHREIBUNG                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Benutzerdefinierter Aktionstyp 5](custom-action-type-5.md)   | JScript-Datei, die in einem binären Tabellenstream gespeichert ist.                                                  |
| [Benutzerdefinierter Aktionstyp 21](custom-action-type-21.md) | JScript-Datei, die mit einem Produkt installiert wird.                                                 |
| [Benutzerdefinierter Aktionstyp 53](custom-action-type-53.md) | Der von einem Eigenschafts Wert angegebene JScript-Text.                                                    |
| [Benutzerdefinierter Aktionstyp 37](custom-action-type-37.md) | JScript-Text, der in der Ziel Spalte der [CustomAction](customaction-table.md) -Tabelle gespeichert ist.  |
| [Benutzerdefinierter Aktionstyp 6](custom-action-type-6.md)   | VBScript-Datei, die in einem [binären](binary-table.md) Tabellenstream gespeichert ist.                             |
| [Benutzerdefinierter Aktionstyp 22](custom-action-type-22.md) | VBScript-Datei, die mit einem Produkt installiert wird.                                                |
| [Benutzerdefinierter Aktionstyp 54](custom-action-type-54.md) | VBScript-Text, der von einem Eigenschafts Wert angegeben wird.                                                   |
| [Benutzerdefinierter Aktionstyp 38](custom-action-type-38.md) | VBScript-Text, der in der Ziel Spalte der [CustomAction](customaction-table.md) -Tabelle gespeichert ist. |



 

> [!Note]  
> Das Installationsprogramm führt benutzerdefinierte Skript Aktionen direkt aus und verwendet nicht den Windows Script Host. Das **WScript** -Objekt kann nicht in einer benutzerdefinierten Skript Aktion verwendet werden, da dieses Objekt vom Windows Script Host bereitgestellt wird. Objekte im Windows Script Host-Objektmodell können nur in benutzerdefinierten Aktionen verwendet werden, wenn Windows Script Host auf dem Computer installiert ist, indem neue Instanzen des-Objekts mit einem Aufrufen von "anateobject" erstellt werden und die ProgID des Objekts (z. b. "Wscript. Shell") bereitgestellt wird. Abhängig vom Typ der benutzerdefinierten Skript Aktion kann der Zugriff auf einige Objekte und Methoden des Windows Script Host-Objektmodells aus Sicherheitsgründen verweigert werden.

 

Weitere Informationen finden Sie unter [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md) für eine Zusammenfassung aller Typen von benutzerdefinierten Aktionen und deren Codierung in die [CustomAction](customaction-table.md) -Tabelle.

 

 



