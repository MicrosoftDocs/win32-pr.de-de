---
title: Erstellen von Aufgaben Dialogfeldern
description: Ein Aufgaben Dialogfeld wird erstellt und entweder mithilfe der taskdialog-Funktion oder der TaskDialogIndirect-Funktion angezeigt.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036536"
---
# <a name="how-to-create-task-dialogs"></a>Erstellen von Aufgaben Dialogfeldern

Ein Aufgaben Dialogfeld wird erstellt und entweder mithilfe der [**taskdialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) -Funktion oder der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Funktion angezeigt.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="taskdialog"></a>Nenne

Die **taskdialog** -Funktion eignet sich für einfache Dialogfelder, die Textinformationen darstellen und eine Standardauswahl anfordern. Diese Erstellungs Funktion unterstützt keine Status leisten, Kontrollkästchen, Fußzeilen, Schaltflächen zum erweitern/reduzieren, benutzerdefinierte Schaltflächen oder Options Felder.

### <a name="taskdialogindirect"></a>TaskDialogIndirect

Die **TaskDialogIndirect** -Funktion ist leistungsfähiger und unterstützt alle verfügbaren Schnittstellen Elemente und ermöglicht es Ihnen, Ereignisse in einer Rückruf Prozedur zu erfassen, damit die Anwendung eine Statusanzeige aktualisieren oder auf einen Link oder eine Schaltfläche klicken kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Aufgaben Dialog](using-task-dialogs.md)
</dt> </dl>

 

 




