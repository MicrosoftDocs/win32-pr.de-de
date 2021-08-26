---
description: Einige der Im Systemsteuerung gefundenen Systemelemente sind erweiterbar. Um eine Systemsteuerung Erweiterung zu installieren, registrieren Sie Ihre Shellerweiterung wie folgt, wobei name der vordefinierte Name des Systemelements ist (siehe Tabelle unten).
title: Erweitern von System Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b4cb426c245c73b6644a95e45d7e2577b4f85f6ed7a28980894183854c1b26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942990"
---
# <a name="extending-system-control-panel-items"></a>Erweitern von System Systemsteuerung Elementen

Einige der Im Systemsteuerung gefundenen Systemelemente sind erweiterbar. Um eine Systemsteuerung Erweiterung zu installieren, registrieren Sie Ihre Shellerweiterung wie folgt, wobei *name* der vordefinierte Name des Systemelements ist (siehe Tabelle unten).

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

Dies ähnelt der Art und Weise, wie Sie eine Erweiterung für ein vordefiniertes Shellobjekt registrieren würden. Da die einzigen Shellerweiterungen, die von Systemsteuerung Elementen unterstützt werden, Eigenschaftenblätter sind, muss sich die Registrierung unter dem \\ **Shellex-Unterschlüssel PropertySheetHandlers** befinden.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Systemsteuerung Element</th>
<th><em>name</em></th>
<th>Hinweise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Anzeige</td>
<td>Schreibtisch</td>
<td>Unterstützt auch das Ersetzen der <strong>Desktopseite.</strong>
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Anzeigen Einstellungen Erweitert</td>
<td>Gerät</td>
<td>Nichthardwarespezifische erweiterte Eigenschaften.
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Anzeigen Einstellungen Erweitert</td>
<td>Anzeige</td>
<td>Hardwarespezifische erweiterte Eigenschaften.
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Internetoptionen</td>
<td>Internet</td>
<td>Die maximale Anzahl von Erweiterungsseiten beträgt 18.</td>
</tr>
<tr class="odd">
<td>Tastatur</td>
<td>Tastatur</td>
<td>Die maximale Anzahl von Erweiterungsseiten beträgt 30.</td>
</tr>
<tr class="even">
<td>Maus</td>
<td>Maus</td>
<td>Unterstützt auch das Ersetzen von Standardseiten. Die maximale Anzahl von Erweiterungsseiten beträgt 8.</td>
</tr>
<tr class="odd">
<td>Energieoptionen</td>
<td>Power</td>
<td>Die maximale Anzahl von Seiten, einschließlich Standardseiten, beträgt 18.</td>
</tr>
<tr class="even">
<td>System</td>
<td>System</td>
<td>Die maximale Anzahl von Erweiterungsseiten beträgt 8.
<blockquote>
[!Note]<br />
Dies wird unter Windows Vista nicht mehr unterstützt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Das Element **Software im** Windows XP-Systemsteuerung ist kein Eigenschaftenblatt und kann daher nicht durch die hier beschriebenen Methoden erweitert werden. Stattdessen wird der Inhalt von Anwendungsverlegern abgerufen. Weitere Informationen zum Hinzufügen von Inhalten zum **Hinzufügen oder Entfernen von Programmen** finden Sie unter [**IAppPublisher,**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher) [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)und [**IPublishedApp.**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Items](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[Registrieren von Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPLApplet](using-cplapplet.md)
</dt> <dt>

[Systemsteuerung der Nachrichtenverarbeitung](message-processing.md)
</dt> <dt>

[Ausführen von Systemsteuerung Elementen](executing-control-panel-items.md)
</dt> <dt>

[Zuweisen Systemsteuerung Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für ein Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




