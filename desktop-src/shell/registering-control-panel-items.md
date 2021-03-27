---
description: System Steuerungselemente müssen registriert werden, damit Sie im Fenster "Systemsteuerung" angezeigt werden.
title: System Steuerungselemente werden registriert
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131844"
---
# <a name="registering-control-panel-items"></a>System Steuerungselemente werden registriert

System Steuerungselemente müssen registriert werden, damit Sie im Fenster "Systemsteuerung" angezeigt werden. Wenn das System Steuerungselement als Teil einer exe-Datei implementiert ist, wird es als Befehls Objekt registriert. Die Registrierung unterscheidet sich, wenn das Element als DLL-Datei implementiert ist, die die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion exportiert.

Bestimmte Anforderungen werden in den folgenden Themen behandelt:

-   [Registrieren von ausführbaren System Steuerungselementen](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Registrieren von dll-System Steuerungselementen](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
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
</dt> <dt>

[Zugreifen auf die Systemsteuerung im abgesicherten Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
