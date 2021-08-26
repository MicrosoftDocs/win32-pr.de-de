---
description: Einige der Systemelemente, die sich in der Systemsteuerung befinden, sind erweiterbar. Um eine Systemsteuerung zu installieren, registrieren Sie Ihre Shell-Erweiterung wie folgt, wobei name der vordefinierte Name des Systemelements ist (siehe Tabelle unten).
title: Erweitern von Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8c5948ad99111dc87578dfa15c5278cf03d5918e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469747"
---
# <a name="extending-system-control-panel-items"></a>Erweitern von Systemsteuerung Elementen

Einige der Systemelemente, die sich in der Systemsteuerung befinden, sind erweiterbar. Um eine Systemsteuerung zu installieren, registrieren Sie Ihre Shell-Erweiterung wie folgt, wobei *name* der vordefinierte Name des Systemelements ist (siehe Tabelle unten).

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

Dies ähnelt der Art und Weise, wie Sie eine Erweiterung für ein vordefiniertes Shell-Objekt registrieren würden. Da die einzigen Shellerweiterungen, die von Systemsteuerung unterstützt werden, Eigenschaftenblätter sind, muss sich die Registrierung unter dem  \\ **Shellex-Unterschlüssel PropertySheetHandlers** befinden.




| Systemsteuerung Element | <em>name</em> | Hinweise | 
|--------------------|---------------|---------|
| Anzeige | Schreibtisch | Unterstützt auch das Ersetzen der <strong>Desktopseite.</strong><blockquote>[!Note]<br />Dies wird unter Windows Vista nicht mehr unterstützt.</blockquote><br /> | 
| Anzeigen Einstellungen Erweitert | Gerät | Nichthardwarespezifische erweiterte Eigenschaften.<blockquote>[!Note]<br />Dies wird unter Windows Vista nicht mehr unterstützt.</blockquote><br /> | 
| Anzeigen Einstellungen Erweitert | Anzeige | Hardwarespezifische erweiterte Eigenschaften.<blockquote>[!Note]<br />Dies wird unter Windows Vista nicht mehr unterstützt.</blockquote><br /> | 
| Internetoptionen | Internet | Die maximale Anzahl von Erweiterungsseiten beträgt 18. | 
| Tastatur | Tastatur | Die maximale Anzahl von Erweiterungsseiten beträgt 30. | 
| Maus | Maus | Unterstützt auch das Ersetzen von Standardseiten. Die maximale Anzahl von Erweiterungsseiten beträgt 8. | 
| Energieoptionen | Strom | Die maximale Anzahl von Seiten, einschließlich Standardseiten, beträgt 18. | 
| System | System | Die maximale Anzahl von Erweiterungsseiten beträgt 8.<blockquote>[!Note]<br />Dies wird unter Windows Vista nicht mehr unterstützt.</blockquote><br /> | 




 

Das **Element Programme hinzufügen oder** entfernen im Windows XP Systemsteuerung ist kein Eigenschaftenblatt und kann daher nicht durch die hier erläuterten Methoden erweitert werden. Stattdessen wird der Inhalt von Anwendungsherausgebern erhalten. Weitere Informationen zum Hinzufügen von Inhalt zu **"Software"** finden Sie unter [**IAppPublisher,**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher) [**IEnumPublishedApps**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)und [**IPublishedApp.**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Elemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
</dt> <dt>

[Registrieren Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPLApplet](using-cplapplet.md)
</dt> <dt>

[Systemsteuerung Nachrichtenverarbeitung](message-processing.md)
</dt> <dt>

[Ausführen Systemsteuerung Elementen](executing-control-panel-items.md)
</dt> <dt>

[Zuweisen Systemsteuerung Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




