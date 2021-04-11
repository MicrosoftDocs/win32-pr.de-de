---
description: In der Registrierungs Tabelle und den zugehörigen Tabellen der Installations Datenbank sind die Registrierungsinformationen enthalten, die die Anwendung in der Systemregistrierung benötigt.
ms.assetid: e4695018-e9c3-400c-b4bb-6160e154d2cf
title: Registrierungsinformationen werden hinzugefügt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb299116b4e5c567d1e1f4b18f23c1e5b0447fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959544"
---
# <a name="adding-registry-information"></a>Registrierungsinformationen werden hinzugefügt

In der [Registrierungs Tabelle](registry-table.md)und den zugehörigen Tabellen der Installations Datenbank sind die Registrierungsinformationen enthalten, die die Anwendung in der Systemregistrierung benötigt. Weitere Informationen finden Sie in der [Gruppe Registrierungs Tabellen](registry-tables-group.md). In diesem Abschnitt fügen Sie die Informationen, die auf dem Computer des Benutzers registriert werden sollen, über das Notepad-Beispiel hinzu.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die leere Registrierungs Tabelle ein.

[Registrierungs Tabelle](registry-table.md)



| Registrierung       | Root | Schlüssel                                 | Name             | Wert    | Komponente\_ |
|----------------|------|-------------------------------------|------------------|----------|-------------|
| CharSet        | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LF charset        | \#0      | Editor     |
| ClipPrecision  | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LF ClipPrecision  | \#2      | Editor     |
| Vorschub     | 2    | Software \\ Microsoft \\ Notepad-Beispiel | lffacename       | Fixedsys | Editor     |
| Kursiv         | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LFI         | \#0      | Editor     |
| Orientation    | 2    | Software \\ Microsoft \\ Notepad-Beispiel | lforientation    | \#0      | Editor     |
| Ausgehende Genauigkeit   | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LF OutPrecision   | \#1      | Editor     |
| Pgesettings   | 2    | Software \\ Microsoft \\ Notepad-Beispiel | fsavepgesete | \#0      | Editor     |
| PitchAndFamily | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LF PitchAndFamily | \#49     | Editor     |
| PointSize      | 2    | Software \\ Microsoft \\ Notepad-Beispiel | ipointsize       | \#120    | Editor     |
| Qualität        | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LF-Qualität        | \#2      | Editor     |
| Durchgestrichen      | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LF Strip-out      | \#0      | Editor     |
| Weight         | 2    | Software \\ Microsoft \\ Notepad-Beispiel | LF Weight         | \#400    | Editor     |
| Umschließen           | 2    | Software \\ Microsoft \\ Notepad-Beispiel | Umbruch            | \#0      | Editor     |



 

[Fortsetzen](specifying-shortcuts.md)

 

 



