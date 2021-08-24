---
description: Eine benutzerdefinierte Aktion kann Funktionen aufrufen, die in VBScript oder JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49e1863d43956e8ec799e467d8391873458d1879f78455abda9ee06fb739aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041370"
---
# <a name="scripts"></a>Skripts

Eine benutzerdefinierte Aktion kann Funktionen aufrufen, die in VBScript oder JScript. Windows Das Installationsprogramm stellt die Skript-Engine nicht zur Verfügung. Autoren, die während der Installation eine Skriptsprache verwenden möchten, müssen daher sicherstellen, dass die entsprechende Skript-Engine verfügbar ist.

Das Installationsprogramm unterstützt keine JScript 1.0.

Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss explizit als benutzerdefinierte 64-Bit-Aktion markiert werden, indem das **msidbCustomActionType64BitScript-Bit** dem numerischen Typ der benutzerdefinierten Aktionen in der Spalte Type der [CustomAction-Tabelle](customaction-table.md) hinzugefügt wird. Weitere Informationen finden Sie unter [Benutzerdefinierte 64-Bit-Aktionen.](64-bit-custom-actions.md)

Die folgenden grundlegenden benutzerdefinierten Aktionstypen rufen funktionen auf, die im Skript geschrieben sind.



| Benutzerdefinierter Aktionstyp                                 | BESCHREIBUNG                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Benutzerdefinierter Aktionstyp 5](custom-action-type-5.md)   | JScript in einem binären Tabellenstream gespeicherte Datei.                                                  |
| [Benutzerdefinierter Aktionstyp 21](custom-action-type-21.md) | JScript, die mit einem Produkt installiert ist.                                                 |
| [Benutzerdefinierter Aktionstyp 53](custom-action-type-53.md) | JScript text, der durch einen Eigenschaftswert angegeben wird.                                                    |
| [Benutzerdefinierter Aktionstyp 37](custom-action-type-37.md) | JScript text, der in der Spalte Target der [CustomAction-Tabelle gespeichert](customaction-table.md) ist.  |
| [Benutzerdefinierter Aktionstyp 6](custom-action-type-6.md)   | VBScript-Datei, die in einem [Binärtabellenstream](binary-table.md) gespeichert ist.                             |
| [Benutzerdefinierter Aktionstyp 22](custom-action-type-22.md) | VBScript-Datei, die mit einem Produkt installiert wird.                                                |
| [Benutzerdefinierter Aktionstyp 54](custom-action-type-54.md) | DURCH einen Eigenschaftswert angegebener VBScript-Text.                                                   |
| [Benutzerdefinierter Aktionstyp 38](custom-action-type-38.md) | VBScript-Text, der in der Spalte Target der [CustomAction-Tabelle gespeichert](customaction-table.md) ist. |



 

> [!Note]  
> Das Installationsprogramm führt benutzerdefinierte Skriptaktionen direkt aus und verwendet Windows Skripthost. Das **WScript-Objekt** kann nicht in einer benutzerdefinierten Skriptaktion verwendet werden, da dieses Objekt vom Skripthost Windows wird. Objekte im Windows Script Host-Objektmodell können nur in benutzerdefinierten Aktionen verwendet werden, wenn der Windows-Skripthost auf dem Computer installiert ist, indem neue Instanzen des Objekts mit einem Aufruf von CreateObject erstellt und die ProgId des Objekts (z. B. "WScript.Shell") zur Verfügung steht. Je nach Typ der benutzerdefinierten Skriptaktion kann der Zugriff auf einige Objekte und Methoden des Windows Script Host-Objektmodells aus Sicherheitsgründen verweigert werden.

 

Weitere Informationen finden [](summary-list-of-all-custom-action-types.md) Sie unter Zusammenfassungsliste aller benutzerdefinierten Aktionstypen, um eine Zusammenfassung aller Typen von benutzerdefinierten Aktionen und deren Codierung in der [CustomAction-Tabelle](customaction-table.md) zu erhalten.

 

 



