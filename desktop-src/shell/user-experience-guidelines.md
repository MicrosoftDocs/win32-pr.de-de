---
description: Die Hauptaufgabe jedes Systemsteuerung Elements besteht darin, ein Fenster anzuzeigen, in dem der Benutzer Einstellungen anzeigen und bearbeiten kann.
title: Richtlinien zur Benutzerfreundlichkeit
ms.topic: article
ms.date: 09/24/2020
ms.assetid: f03a154b-9781-4718-8244-3d57fee0755e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 15ef54d44a466f3c766075eae771ccac9d74e20c0622d6092530f1015a538425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857079"
---
# <a name="user-experience-guidelines"></a>Richtlinien zur Benutzerfreundlichkeit

Die Hauptaufgabe jedes Systemsteuerung Elements besteht darin, ein Fenster anzuzeigen, in dem der Benutzer Einstellungen anzeigen und bearbeiten kann. Informationen zum Verhalten und Design von Systemsteuerung Elementen finden Sie in den Richtlinien zur Benutzeroberfläche [(Control Panels User Experience, UX).](../uxguide/winenv-ctrl-panels.md) Die in diesem Thema erläuterten Richtlinien zeigen eine Aufgabenflussmethode zum Organisieren eines Systemsteuerung Elements. Dadurch werden die wichtigsten Einstellungen auf einer Startseite platziert. Weniger häufig verwendete Einstellungen werden auf Spoke-Seiten platziert oder über Links in einem Seitenbereich aufgerufen.

Die Systemsteuerung enthält viele Elemente, die diesen Richtlinien entsprechen, z. B. Center für erleicherte Bedienung und Netzwerk- und Freigabecenter. Andere Systemsteuerung Elemente verwenden das Eigenschaftenblattformat des Dialogfelds im Registerkartenformat wie in früheren Versionen von Windows. Beispiele hierfür sind das Element Maus und Internetoptionen. Die Verwendung des Eigenschaftenblattformats sollte eingestellt werden. Wenn Sie neue Systemsteuerung Elemente erstellen, sollten Sie die Richtlinien für den Taskflow befolgen.

In der Vergangenheit wurden Systemsteuerung Elemente als .cpl-Dateien gepackt. Dies ist nicht mehr erforderlich. Neue Systemsteuerung Elemente sollten als eigenständige .exe datei oder als Befehlszeilenflagsoption für die ausführbare Hauptdatei der Anwendung implementiert werden.

> [!Note]  
> Auf 64-Bit-Systemen werden 32-Bit-Systemsteuerung Elemente im Systemsteuerung angezeigt, wenn die **Ordneroption 32-Bit-Systemsteuerung Elemente anzeigen** ausgewählt ist. Die 32-Bit-Elemente müssen sich im Ordner %SystemRoot% \\ SysWOW64 befinden, um angezeigt zu werden. Sie erfordern keine weitere Registrierung.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Systemsteuerung Items](control-panel-applications.md)
</dt> <dt>

[Registrieren von Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Verwenden von CPLApplet](using-cplapplet.md)
</dt> <dt>

[Systemsteuerung der Nachrichtenverarbeitung](message-processing.md)
</dt> <dt>

[Ausführen von Systemsteuerung Elementen](executing-control-panel-items.md)
</dt> <dt>

[Erweitern von System Systemsteuerung Elementen](extending-system-control-panel-items.md)
</dt> <dt>

[Zuweisen Systemsteuerung Kategorien](assigning-control-panel-categories.md)
</dt> <dt>

[Erstellen durchsuchbarer Aufgabenlinks für ein Systemsteuerung Element](creating-searchable-task-links.md)
</dt> <dt>

[Zugreifen auf die Systemsteuerung im Tresor-Modus](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



