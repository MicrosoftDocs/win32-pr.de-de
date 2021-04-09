---
description: Nicht verzögerte benutzerdefinierte Aktionen, die Dynamic Link Libraries oder Skripts aufrufen, können auf eine laufende Installation zugreifen, um die Attribute der aktuellen Installationssitzung abzufragen oder zu ändern.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959555"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion

Nicht verzögerte benutzerdefinierte Aktionen, die [Dynamic Link Libraries](dynamic-link-libraries.md) oder [Skripts](scripts.md) aufrufen, können auf eine laufende Installation zugreifen, um die Attribute der aktuellen Installationssitzung abzufragen oder zu ändern. Nur ein **Sitzungs** Objekt kann für jeden Prozess vorhanden sein, und benutzerdefinierte Aktions Skripts dürfen nicht versuchen, eine weitere Sitzung zu erstellen.

Benutzerdefinierte Aktionen können nur temporäre Zeilen, Spalten oder Tabellen aus einer Datenbank hinzufügen, ändern oder entfernen. Benutzerdefinierte Aktionen können keine persistenten Daten in einer Datenbank ändern, z. b. Daten, die Teil der Datenbank sind, die auf dem Datenträger gespeichert ist.

[Dynamic Link Libraries](dynamic-link-libraries.md)

Für den Zugriff auf eine ausgeführte Installation werden benutzerdefinierte Aktionen, die dll (Dynamic Link Libraries) aufrufen, als einziges Argument des msihandle-Typs für die aktuelle Sitzung als einziges Argument für den DLL-Einstiegspunkt, der in der Ziel Spalte der [Tabelle CustomAction](customaction-table.md)benannt ist Da das Installationsprogramm dieses Handle bereitstellt, sollte es von der benutzerdefinierten Aktion nicht geschlossen werden, um z. b. das Handle *hinstall* vom Installationsprogramm zu empfangen, wird die benutzerdefinierte Action-Funktion wie folgt deklariert.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Für den schreibgeschützten Zugriff auf die aktuelle Datenbank erhalten Sie das Daten Bank Handle durch Aufrufen von [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase). Weitere Informationen finden Sie unter Abrufen [eines Daten Bank Handles](obtaining-a-database-handle.md).

[Skripts](scripts.md)

In VBScript oder JScript geschriebene benutzerdefinierte Aktionen können mithilfe des [**Session-Objekts**](session-object.md)auf die aktuelle Installationssitzung zugreifen. Das Installationsprogramm erstellt ein **Sitzungs** Objekt mit dem Namen "Session", das auf die aktuelle Installation verweist. Verwenden Sie für den schreibgeschützten Zugriff auf die aktuelle Datenbank die [**Database**](session-database.md) -Eigenschaft des **Session** -Objekts.

Da ein Skript aus dem Kontext des [**Session**](session-object.md) -Objekts ausgeführt wird, ist es nicht immer erforderlich, Eigenschaften und Methoden vollständig zu qualifizieren. Im folgenden Beispiel kann die Me-Referenz beim Verwenden von VBScript das **Session** -Objekt ersetzen, z. b. sind die folgenden drei Zeilen gleichwertig.


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

Sie können nicht über benutzerdefinierte Aktionen auf die aktuelle Installer-Sitzung zugreifen, die ausführbare Dateien aufrufen, die mit einer Befehlszeile gestartet wurden, z. b. [benutzerdefinierter Aktionstyp 2](custom-action-type-2.md) und [benutzerdefinierter Aktionstyp 18](custom-action-type-18.md).

[Benutzerdefinierte Aktionen für verzögerte Ausführung](deferred-execution-custom-actions.md)

Sie können nicht auf die aktuelle Installer-Sitzung oder auf alle Eigenschaften Daten aus einer benutzerdefinierten Aktion für eine verzögerte Ausführung zugreifen. Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



