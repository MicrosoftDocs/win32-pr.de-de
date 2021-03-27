---
description: Die Hauptverantwortung für alle System Steuerungselemente besteht darin, ein Fenster anzuzeigen, in dem der Benutzereinstellungen anzeigen und bearbeiten kann.
title: Richtlinien zur Benutzerfreundlichkeit
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e25f8885c2444a51d5d5d8cc917121c7f3b26a09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995102"
---
# <a name="user-experience-guidelines"></a>Richtlinien zur Benutzerfreundlichkeit

Die Hauptverantwortung für alle System Steuerungselemente besteht darin, ein Fenster anzuzeigen, in dem der Benutzereinstellungen anzeigen und bearbeiten kann. Weitere Informationen zum Verhalten und zum Entwurf von System Steuerungselementen finden Sie in den [Richtlinien zur Benutzerfreundlichkeit](../uxguide/winenv-ctrl-panels.md) in den Steuerungs Bereichen. Die in diesem Thema erläuterten Richtlinien zeigen eine Aufgaben Fluss Methode zum Organisieren eines System Steuerungs Elements. Dadurch werden die wichtigsten Einstellungen auf einer Startseite platziert. Weniger häufig verwendete Einstellungen werden auf der Seite "Sprachanrufe" platziert, oder der Zugriff erfolgt über Links in einem Seitenbereich.

Die Systemsteuerung umfasst viele Elemente, die diese Richtlinien einhalten, wie z. b. das Easy Access Center und das Netzwerk-und Freigabe Center. Andere System Steuerungselemente verwenden das Format des Dialogfeld Eigenschaften Blatts im Registerkarten Format, wie in früheren Versionen von Windows. Beispiele hierfür sind die Maus Element-und Internet Optionen. Die Verwendung des Eigenschaften Blatt Formats sollte eingestellt werden. Wenn Sie neue System Steuerungselemente erstellen, befolgen Sie die Richtlinien für den Task Ablauf.

In der Vergangenheit wurden System Steuerungselemente als cpl-Dateien verpackt. Dies ist nicht mehr erforderlich. Neue System Steuerungselemente müssen als eigenständige exe-Datei oder als befehlszeilenflag für die ausführbare Hauptdatei der Anwendung implementiert werden.

> [!Note]  
> Auf 64-Bit-Systemen werden in der Systemsteuerung die System Steuerungselemente 32-Bit angezeigt, wenn die Option " **32-Bit-System Steuerungselemente anzeigen** " ausgewählt ist. Die 32-Bit-Elemente müssen sich im Ordner% systemroot% \\ syswow64 befinden, der angezeigt werden soll. Sie erfordern keine weitere Registrierung.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente](control-panel-applications.md)
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
</dt> <dt>

[Zugreifen auf die Systemsteuerung im abgesicherten Modus](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



