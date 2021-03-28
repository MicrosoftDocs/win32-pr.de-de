---
description: Einige der in der Systemsteuerung gefundenen Systemelemente sind erweiterbar. Um eine System Steuerungs Erweiterung zu installieren, registrieren Sie Ihre Shellerweiterung wie folgt, wobei Name der vordefinierte Name des System Elements ist (siehe Tabelle unten).
title: Erweitern von System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993870"
---
# <a name="extending-system-control-panel-items"></a>Erweitern von System Steuerungselementen

Einige der in der Systemsteuerung gefundenen Systemelemente sind erweiterbar. Um eine System Steuerungs Erweiterung zu installieren, registrieren Sie Ihre Shellerweiterung wie folgt, wobei *Name* der vordefinierte Name des System Elements ist (siehe Tabelle unten).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

Dies ähnelt der Art und Weise, wie Sie eine Erweiterung für ein vordefiniertes Shellobjekt registrieren würden. Da es sich bei den einzigen Shellerweiterungen, die von System Steuerungselementen unterstützt werden, um Eigenschaften Blätter handelt, muss die Registrierung unter dem Unterschlüssel **shellex** \\ **propertysheethandlers** abgelegt werden.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>System Steuerungselement</th>
<th><em>name</em></th>
<th>Bemerkungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Anzeige</td>
<td>Schreibtisch</td>
<td>Unterstützt auch die Ersetzung der <strong>Desktop</strong> Seite.
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Anzeigeeinstellungen erweitert</td>
<td>Sicherungsmedium</td>
<td>Nicht Hardware spezifische erweiterte Eigenschaften.
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Anzeigeeinstellungen erweitert</td>
<td>Anzeige</td>
<td>Hardware spezifische erweiterte Eigenschaften.
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Internetoptionen</td>
<td>Internet</td>
<td>Die maximal zulässige Anzahl von Erweiterungs Seiten ist 18.</td>
</tr>
<tr class="odd">
<td>Tastatur</td>
<td>Tastatur</td>
<td>Die maximal zulässige Anzahl von Erweiterungs Seiten ist 30.</td>
</tr>
<tr class="even">
<td>Maus</td>
<td>Maus</td>
<td>Unterstützt auch das Ersetzen von Standardseiten. Die maximal zulässige Anzahl von Erweiterungs Seiten ist 8.</td>
</tr>
<tr class="odd">
<td>Energieoptionen</td>
<td>Power</td>
<td>Die maximale Anzahl von Seiten, einschließlich Standardseiten, ist 18.</td>
</tr>
<tr class="even">
<td>System</td>
<td>System</td>
<td>Die maximal zulässige Anzahl von Erweiterungs Seiten ist 8.
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Das **Element "** Software" in der Windows XP-Systemsteuerung ist kein Eigenschaften Blatt und kann daher nicht durch die hier beschriebenen Methoden erweitert werden. Stattdessen wird der Inhalt von Anwendungs Verlegern abgerufen. Weitere Informationen zum Hinzufügen von Inhalten zum **Hinzufügen oder Entfernen von Programmen finden Sie** unter [**iapppublisher**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**ienumpublishedapps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)und [**ipublishedapp**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPlApplet](using-cplapplet.md)
</dt> <dt>

[Nachrichtenverarbeitung in der Systemsteuerung](message-processing.md)
</dt> <dt>

[Ausführen von System Steuerungselementen](executing-control-panel-items.md)
</dt> <dt>

[Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




