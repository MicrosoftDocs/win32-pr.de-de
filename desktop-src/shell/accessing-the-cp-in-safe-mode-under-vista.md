---
description: Standardmäßig werden ab Windows Vista Systemsteuerung elemente nicht angezeigt, wenn Windows im abgesicherten Modus ausgeführt wird.
title: Zugreifen auf die Systemsteuerung im Tresor Modus
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 777a44c7fe30b0481096a1c5d62c98410277a3bc76169925aff4ae5e59e549d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710790"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Zugreifen auf die Systemsteuerung im Tresor Modus

Standardmäßig werden ab Windows Vista Systemsteuerung elemente nicht angezeigt, wenn Windows im abgesicherten Modus ausgeführt wird. Damit ein neues Systemsteuerung im abgesicherten Modus angezeigt werden kann, können für den Elementtyp geeignete Registrierungswerte festgelegt werden. Die Werte werden wie folgt interpretiert:



| Wert | Bedeutung                                                            |
|-------|--------------------------------------------------------------------|
| 1     | Das Element sollte nur im minimal sicheren Modus angezeigt werden.                  |
| 2     | Das Element sollte nur dann im abgesicherten Modus angezeigt werden, wenn das Netzwerk aktiviert ist. |
| 3     | Das Element sollte immer in einer beliebigen Form des abgesicherten Modus angezeigt werden.            |



 

Dieses Beispiel zeigt die Einträge, die für ein Element erforderlich sind, das als .cpl oder .dll implementiert wird. Sie gibt an, dass das Element im abgesicherten Modus mit Netzwerk angezeigt werden soll.

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

Dieses Beispiel zeigt die Einträge, die für ein Element erforderlich sind, das als .exe implementiert ist. Sie gibt an, dass das Element in einer beliebigen Form des abgesicherten Modus angezeigt werden soll.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

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

[Erweitern von Systemsteuerung Elementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen Systemsteuerung Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für ein Systemsteuerung Element](creating-searchable-task-links.md)
</dt> </dl>

 

 



