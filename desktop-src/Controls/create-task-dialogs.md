---
title: Erstellen von Aufgabendialogfeldern
description: Ein Aufgabendialogfeld wird mithilfe der TaskDialog-Funktion oder der TaskDialogIndirect-Funktion erstellt und angezeigt.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6f74f1922330cae1550fda1a9ad6d451221452017f3856ae5e859948019828
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504020"
---
# <a name="how-to-create-task-dialogs"></a>Erstellen von Aufgabendialogfeldern

Ein Aufgabendialogfeld wird mithilfe der [**TaskDialog-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) oder der [**TaskDialogIndirect-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) erstellt und angezeigt.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="taskdialog"></a>TaskDialog

Die **TaskDialog-Funktion** eignet sich für einfache Dialogfelder, die Textinformationen darstellen und nach einer Standardauswahl fragen. Diese Erstellungsfunktion unterstützt keine Statusleisten, Kontrollkästchen, Fußzeilen, Schaltflächen zum Erweitern/Reduzieren, benutzerdefinierte Schaltflächen oder Optionsfelder.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

Die **TaskDialogIndirect-Funktion** ist leistungsfähiger und unterstützt alle verfügbaren Schnittstellenelemente und ermöglicht Es Ihnen auch, Ereignisse in einer Rückrufprozedur zu erfassen, sodass Ihre Anwendung eine Statusanzeige aktualisieren oder auf einen Klick auf einen Link oder eine Schaltfläche reagieren kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Aufgabendialogfeldern](using-task-dialogs.md)
</dt> </dl>

 

 




