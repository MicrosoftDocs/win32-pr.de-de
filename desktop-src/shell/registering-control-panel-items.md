---
description: Systemsteuerung Elemente müssen registriert werden, damit sie im Fenster Systemsteuerung werden.
title: Registrieren Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: daa86bfd9975df5cd057dd3e577f443bafa6c363061e267e67adad69b590e678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661080"
---
# <a name="registering-control-panel-items"></a>Registrieren Systemsteuerung Elementen

Systemsteuerung Elemente müssen registriert werden, damit sie im Fenster Systemsteuerung werden. Wenn das Systemsteuerung-Element als Teil einer .exe implementiert wird, wird es als Befehlsobjekt registriert. Die Registrierung unterscheidet sich, wenn das Element als eine .dll implementiert wird, die die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) exportiert.

Spezifische Anforderungen werden in den folgenden Themen erläutert:

-   [Registrieren von ausführbaren Systemsteuerung Elementen](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Registrieren von DLL-Systemsteuerung Elementen](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Elemente](control-panel-applications.md)
</dt> <dt>

[Richtlinien zur Benutzerfreundlichkeit](user-experience-guidelines.md)
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

[Erstellen durchsuchbarer Aufgabenlinks für Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus unter Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
