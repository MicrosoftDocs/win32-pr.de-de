---
description: Nicht standardmäßige benutzerdefinierte Aktionen, die Dynamic Link-Bibliotheken oder Skripts aufrufen, können auf eine ausgeführte Installation zugreifen, um die Attribute der aktuellen Installationssitzung abfragt oder zu ändern.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Zugreifen auf die aktuelle Installersitzung innerhalb einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ee3214b8f8664b57f5216b28a7f5d5269d76049fe5c4dd24f7ab8d130d89a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640189"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Zugreifen auf die aktuelle Installersitzung innerhalb einer benutzerdefinierten Aktion

Nicht standardmäßige benutzerdefinierte Aktionen, die Dynamic [](scripts.md) [Link-Bibliotheken](dynamic-link-libraries.md) oder Skripts aufrufen, können auf eine ausgeführte Installation zugreifen, um die Attribute der aktuellen Installationssitzung abfragt oder zu ändern. Für jeden **Prozess kann** nur ein Sitzungsobjekt vorhanden sein, und benutzerdefinierte Aktionsskripts dürfen nicht versuchen, eine weitere Sitzung zu erstellen.

Benutzerdefinierte Aktionen können einer Datenbank nur temporäre Zeilen, Spalten oder Tabellen hinzufügen, ändern oder daraus entfernen. Benutzerdefinierte Aktionen können keine persistenten Daten in einer Datenbank ändern, z. B. Daten, die Teil der auf dem Datenträger gespeicherten Datenbank sind.

[Dynamic Link Libraries](dynamic-link-libraries.md)

Für den Zugriff auf eine ausgeführte Installation werden benutzerdefinierte Aktionen, die Dynamic Link Libraries (DLL) aufrufen, ein Handle vom Typ MSIHANDLE für die aktuelle Sitzung als einziges Argument an den DLL-Einstiegspunkt übergeben, der in der Spalte Ziel der [CustomAction-Tabelle](customaction-table.md)benannt ist. Da das Installationsprogramm dieses Handle bietet, sollte die benutzerdefinierte Aktion es nicht schließen, z. B. um das Handle *hInstall* vom Installationsprogramm zu empfangen, wird die benutzerdefinierte Aktionsfunktion wie folgt deklariert.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Rufen Sie für den schreibgeschützten Zugriff auf die aktuelle Datenbank das Datenbankhandles ab, indem [**Sie MsiGetActiveDatabase aufrufen.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) Weitere Informationen finden Sie unter [Abrufen eines Datenbankhandpunkts.](obtaining-a-database-handle.md)

[Skripts](scripts.md)

Benutzerdefinierte Aktionen, die in VBScript oder JScript, können mithilfe des Sitzungsobjekts auf die aktuelle [**Installationssitzung zugreifen.**](session-object.md) Das Installationsprogramm erstellt ein **Session-Objekt** namens "Session", das auf die aktuelle Installation verweist. Verwenden Sie für den schreibgeschützten Zugriff auf die aktuelle Datenbank die [**Database-Eigenschaft**](session-database.md) des **Session-Objekts.**

Da ein Skript aus dem Kontext des [**Session-Objekts**](session-object.md) ausgeführt wird, ist es nicht immer erforderlich, Eigenschaften und Methoden vollständig zu qualifizieren. Im folgenden Beispiel kann der Me-Verweis bei Verwendung von VBScript das **Session-Objekt** ersetzen, z. B. sind die folgenden drei Zeilen gleichwertig.


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[Ausführbare Dateien](executable-files.md)

Sie können nicht über benutzerdefinierte Aktionen auf die aktuelle Installersitzung zugreifen, die ausführbare Dateien aufrufen, die über eine Befehlszeile gestartet wurden, z. B. Benutzerdefinierter Aktionstyp [2](custom-action-type-2.md) und [Benutzerdefinierter Aktionstyp 18.](custom-action-type-18.md)

[Benutzerdefinierte Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)

Sie können nicht auf die aktuelle Installersitzung oder alle Eigenschaftendaten einer benutzerdefinierten Aktion mit verzögerter Ausführung zugreifen. Weitere Informationen finden Sie unter [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf eine Datenbank oder Sitzung innerhalb einer benutzerdefinierten Aktion](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



