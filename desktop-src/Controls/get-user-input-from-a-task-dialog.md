---
title: Vorgehensweise beim erhalten von Benutzereingaben über ein Aufgaben Dialogfeld
description: Zum Ausführen einer Aufgabe übermitteln Benutzer die Aufgaben Details an die Anwendung, indem Sie die Steuerelemente im Aufgaben Dialogfeld Konfigurieren und dann auf eine Befehls Schaltfläche klicken (normalerweise OK).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949169"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a>Vorgehensweise beim erhalten von Benutzereingaben über ein Aufgaben Dialogfeld

Zum Ausführen einer Aufgabe übermitteln Benutzer die Aufgaben Details an die Anwendung, indem Sie die Steuerelemente im Aufgaben Dialogfeld Konfigurieren und dann auf eine Befehls Schaltfläche klicken (normalerweise **OK**).

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="getting-user-input-from-a-task-dialog"></a>Erhalten von Benutzereingaben aus einem Aufgaben Dialogfeld

Sie können die Schaltfläche ermitteln, auf die geklickt wurde, indem Sie den *pnbutton* -Parameter der aufrufenden Funktion untersuchen. Sie können auch das ausgewählte Optionsfeld über den Parameter *pnradiobutton* von [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)und den Status des Kontrollkästchens Überprüfung des *pfverificationflagcheck* -Parameters identifizieren.

Ein Klick auf Schaltflächen und Hyperlinks wird von der [*taskdialogcallbackproc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) -Funktion in Form der [ \_ klickschaltfläche \_ "TDN-Schaltfläche](tdn-button-clicked.md) " und von [TDN \_ \_](tdn-hyperlink-clicked.md) -Klicks empfangen. Wenn die Rückruffunktion \_ nach der Behandlung einer Schaltflächen Benachrichtigung S OK zurückgibt, wird das Aufgaben Dialogfeld geschlossen, und der Befehls Bezeichner der Schaltfläche wird in *pnbutton* zurückgegeben. Wenn Sie "false" zurückgeben \_ oder keine Rückruffunktion haben, bleibt das Aufgaben Dialogfeld geöffnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Aufgaben Dialog](using-task-dialogs.md)
</dt> </dl>

 

 