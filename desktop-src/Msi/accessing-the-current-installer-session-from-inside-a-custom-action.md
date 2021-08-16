---
description: Nicht abgeleitete benutzerdefinierte Aktionen, die Dynamic Link-Bibliotheken oder -Skripts aufrufen, können auf eine ausgeführte Installation zugreifen, um die Attribute der aktuellen Installationssitzung abzufragen oder zu ändern.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Zugreifen auf die aktuelle Installersitzung aus einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3ee3214b8f8664b57f5216b28a7f5d5269d76049fe5c4dd24f7ab8d130d89a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640189"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a>Zugreifen auf die aktuelle Installersitzung aus einer benutzerdefinierten Aktion

Nicht abgeleitete benutzerdefinierte Aktionen, die [Dynamic Link-Bibliotheken](dynamic-link-libraries.md) oder [-Skripts](scripts.md) aufrufen, können auf eine ausgeführte Installation zugreifen, um die Attribute der aktuellen Installationssitzung abzufragen oder zu ändern. Für jeden Prozess kann nur ein **Sitzungsobjekt** vorhanden sein, und benutzerdefinierte Aktionsskripts dürfen nicht versuchen, eine weitere Sitzung zu erstellen.

Benutzerdefinierte Aktionen können nur temporäre Zeilen, Spalten oder Tabellen aus einer Datenbank hinzufügen, ändern oder entfernen. Benutzerdefinierte Aktionen können persistente Daten in einer Datenbank nicht ändern, z. B. Daten, die Teil der auf dem Datenträger gespeicherten Datenbank sind.

[Dynamic Link-Bibliotheken](dynamic-link-libraries.md)

Um auf eine ausgeführte Installation zuzugreifen, werden benutzerdefinierte Aktionen, die Dynamic Link Libraries (DLL) aufrufen, als einziges Argument an den DLL-Einstiegspunkt übergeben, der in der Target -Spalte der [CustomAction-Tabelle](customaction-table.md)den Typ MSIHANDLE für die aktuelle Sitzung hat. Da das Installationsprogramm dieses Handle bereitstellt, sollte es von der benutzerdefinierten Aktion nicht geschlossen werden. Um z. B. das Handle *hInstall* vom Installationsprogramm zu empfangen, wird die benutzerdefinierte Aktionsfunktion wie folgt deklariert.


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



Rufen Sie für den schreibgeschützten Zugriff auf die aktuelle Datenbank das Datenbankhandle ab, indem [**Sie MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase)aufrufen. Weitere Informationen finden Sie unter [Abrufen eines Datenbankhandle.](obtaining-a-database-handle.md)

[Skripts](scripts.md)

In VBScript oder JScript geschriebene benutzerdefinierte Aktionen können mithilfe des [**Sitzungsobjekts**](session-object.md)auf die aktuelle Installationssitzung zugreifen. Das Installationsprogramm erstellt ein **Sitzungsobjekt** mit dem Namen "Session", das auf die aktuelle Installation verweist. Verwenden Sie für den schreibgeschützten Zugriff auf die aktuelle Datenbank die [**Database-Eigenschaft**](session-database.md) des **Session-Objekts.**

Da ein Skript im Kontext des [**Session-Objekts**](session-object.md) ausgeführt wird, ist es nicht immer erforderlich, Eigenschaften und Methoden vollständig zu qualifizieren. Im folgenden Beispiel kann der Me-Verweis bei Verwendung von VBScript das **Session-Objekt** ersetzen, z. B. sind die folgenden drei Zeilen gleichwertig.


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

Sie können nicht über benutzerdefinierte Aktionen, die ausführbare Dateien aufrufen, die über eine Befehlszeile gestartet wurden, auf die aktuelle Installersitzung zugreifen, z. B. [benutzerdefinierter Aktionstyp 2](custom-action-type-2.md) und [benutzerdefinierter Aktionstyp 18.](custom-action-type-18.md)

[Benutzerdefinierte Aktionen für verzögerte Ausführung](deferred-execution-custom-actions.md)

Sie können nicht auf die aktuelle Installationsprogrammsitzung oder alle Eigenschaftsdaten aus einer benutzerdefinierten Aktion mit verzögerter Ausführung zugreifen. Weitere Informationen finden Sie unter [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf eine Datenbank oder Sitzung über eine benutzerdefinierte Aktion](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



