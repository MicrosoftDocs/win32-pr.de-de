---
description: Die Beispiel Spezifikationen umfassen das Senden von Action Data-Nachrichten, wenn eine benutzerdefinierte Aktion ein Benutzerkonto erstellt oder entfernt, und meldet einen Fehler, wenn ein Konto nicht erstellt werden kann.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Erstellen der Aktions Text-und Fehler Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864452"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Erstellen der Aktions Text-und Fehler Tabellen

Die Beispiel Spezifikationen umfassen das Senden von Action Data-Nachrichten, wenn eine benutzerdefinierte Aktion ein Benutzerkonto erstellt oder entfernt, und meldet einen Fehler, wenn ein Konto nicht erstellt werden kann.

Geben Sie die folgenden Einträge in die Tabelle "aktiontext" ein, um von den Aktions Textnachrichten verwendete Informationen bereitzustellen.

[Tabelle "aktiontext"](actiontext-table.md)



| Aktion            | BESCHREIBUNG                                                       | Vorlage                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| Processaccounts   | Aktionen zum Erstellen von Benutzerkonten auf dem lokalen Computer werden erzeugt. | Konto: \[ 1 \] , Attribute: \[ 2\] |
| CreateAccount     | Das Benutzerkonto wird auf dem lokalen Computer erstellt.                      | Konto: \[ 1\]                    |
| RemoveAccount     | Das Benutzerkonto wird aus dem lokalen Computer entfernt.                    | Konto: \[ 1\]                    |
| Rollbackaccount   | Rollback der Erstellung von Benutzerkonten auf dem lokalen Computer. | Konto: \[ 1\]                    |
| Nicht installaccounts | Aktionen zum Entfernen von Benutzerkonten auf dem lokalen Computer werden erzeugt. | Konto: \[ 1\]                    |



 

Geben Sie die folgenden Einträge in die Fehler Tabelle ein, um die von der Fehlerberichterstattung verwendeten Informationen bereitzustellen.

[Fehler Tabelle](error-table.md)



| Fehler | `Message`                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | Das Benutzerkonto " \[ 2" kann nicht \] auf dem lokalen Computer erstellt werden. Fehler Code: \[ 3 \] . |
| 25002 | Das Benutzerkonto " \[ 2 \] " ist bereits auf dem lokalen Computer vorhanden.                      |
| 25003 | Das Benutzerkonto " \[ 2 \] " auf dem lokalen Computer kann nicht entfernt werden. Fehler Code: \[ 3 \] . |
| 25004 | Das Benutzerkonto " \[ 2 \] " ist auf dem lokalen Computer nicht vorhanden.                      |



 

Fahren Sie mit [dem Erstellen der InstallExecuteSequence-Tabelle](authoring-the-installexecutesequence-table.md)fort.

 

 



