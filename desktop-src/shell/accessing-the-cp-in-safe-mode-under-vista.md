---
description: Standardmäßig werden ab Windows Vista-System Steuerungselemente nicht angezeigt, wenn Windows im abgesicherten Modus ausgeführt wird.
title: Zugreifen auf die Systemsteuerung im abgesicherten Modus
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977416"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Zugreifen auf die Systemsteuerung im abgesicherten Modus

Standardmäßig werden ab Windows Vista-System Steuerungselemente nicht angezeigt, wenn Windows im abgesicherten Modus ausgeführt wird. Damit ein neues System Steuerungselement im abgesicherten Modus angezeigt werden kann, können für den Elementtyp geeignete Registrierungs Werte festgelegt werden. Die Werte werden wie folgt interpretiert:



| Wert | Bedeutung                                                            |
|-------|--------------------------------------------------------------------|
| 1     | Das Element sollte nur im minimal abgesicherten Modus angezeigt werden.                  |
| 2     | Das Element sollte nur im abgesicherten Modus angezeigt werden, wenn das Netzwerk aktiviert ist. |
| 3     | Das Element sollte immer in beliebiger Form Abgesicherter Modus angezeigt werden.            |



 

Dieses Beispiel zeigt die Einträge, die für ein Element erforderlich sind, das als cpl-oder DLL-Datei implementiert ist. Er gibt an, dass das Element im abgesicherten Modus mit Netzwerk angezeigt werden soll.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

Dieses Beispiel zeigt die Einträge, die für ein Element erforderlich sind, das als exe-Datei implementiert ist. Gibt an, dass das Element in beliebiger Form Abgesicherter Modus angezeigt werden soll.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

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

[Erweitern von System Steuerungselementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md)
</dt> </dl>

 

 



