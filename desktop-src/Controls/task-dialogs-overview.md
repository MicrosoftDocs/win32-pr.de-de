---
title: Informationen zu Taskdialogfeldern
description: Bei einem Aufgabendialogfeld handelt es sich um ein Dialogfeld zum Anzeigen von Informationen und zum Entgegennehmen einfacher Eingaben des Benutzers.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2367e3cadff68f10af9d883d4ed7959e4e862a6f406a83361ea2f40b2f69c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061428"
---
# <a name="about-task-dialogs"></a>Informationen zu Taskdialogfeldern

Bei einem Aufgabendialogfeld handelt es sich um ein Dialogfeld zum Anzeigen von Informationen und zum Entgegennehmen einfacher Eingaben des Benutzers. Wie ein Meldungsfeld wird es vom Betriebssystem entsprechend den von Ihnen festgelegten Parametern formatiert. Ein Aufgabendialogfeld verfügt jedoch über viel mehr Funktionen als ein Meldungsfeld.

> [!Note]  
> Taskdialogfelder erfordern das Singlethread-Apartmentmodell (STA).

 

## <a name="parts-of-a-task-dialog"></a>Teile eines Aufgabendialogfelds

Ein Aufgabendialog besteht aus mehreren Elementen, von denen die meisten optional sind. Die folgende Abbildung zeigt die verschiedenen Teile eines Aufgabendialogfelds.

![Screenshot eines Fensters mit verschiedenen Schaltflächen, einschließlich eines neben reduzierten Steuerelementtexts](images/taskdialog.jpg)

In der folgenden Abbildung hat der Benutzer auf die Schaltfläche neben dem reduzierten Steuerelementtext geklickt, sodass dort und in der Fußzeile alternativer Text angezeigt wird.

![Screenshot des vorherigen Fensters, aber mit zwei Zeilen erweitertem Steuerelementtext](images/taskdialogexpand.jpg)

Die Abbildungen zeigen die folgenden Teile:



| Teil                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          | TASKDIALOGCONFIG-Mitglied                                    |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Fenstertitel           | Beschriftung des Fensters.                                                                                                                                                                                                                                                                                                                                                               | **pszWindowTitle**                                         |
| Hauptsymbol              | Ein großes Symbol, das den Zweck des Aufgabendialogfelds andeutet.                                                                                                                                                                                                                                                                                                                          | **hMainIcon** oder **pszMainIcon**                           |
| Main-Anweisung       | Prinzipaltext.                                                                                                                                                                                                                                                                                                                                                                      | **pszMainInstruction**                                     |
| Content                | Zusätzlicher Text.                                                                                                                                                                                                                                                                                                                                                                          | **pszContent**                                             |
| Statusleiste           | Eine animierte Leiste, die den Fortschritt einer Aufgabe zeigt.                                                                                                                                                                                                                                                                                                                                | **dwFlags**                                                |
| Optionsfelder          | Anwendungsdefinierte Optionen für den Benutzer.                                                                                                                                                                                                                                                                                                                                            | **pRadioButtons**                                          |
| Benutzerdefinierte Schaltfläche          | Eine Schaltfläche, die keine der gängigen Schaltflächen ist. Dies kann entweder eine normale Schaltfläche oder, wie in der Abbildung dargestellt, ein Befehlslink mit bis zu zwei Textzeilen sein.                                                                                                                                                                                                                    | **pButtons**                                               |
| Schaltfläche "Erweitern/Reduzieren&quot; | Eine Schaltfläche, die verwendet werden kann, um zwischen dem anwendungsdefinierten reduzierten Steuerelementtext (z. B. &quot;Weitere Details anzeigen") und dem erweiterten Steuerelementtext, der in zwei oder mehr Zeilen angezeigt werden kann, umschalten zu können. Wenn der Steuerelementtext erweitert wird, wird der zusätzliche Text in **pszExpandedInformation** ebenfalls angezeigt, entweder nach dem Inhaltstext oder (wie in der zweiten Abbildung dargestellt) in der Fußzeile. | **pszCollapsedControlText** und **pszExpandedControlText** |
| Kontrollkästchen "Überprüfung" | Ein Kontrollkästchen, das von anwendungsdefiniertm Text für einfache Optionen wie "Dieses Dialogfeld nicht mehr anzeigen" begleitet wird.                                                                                                                                                                                                                                                                     | **pszVerificationText**                                    |
| Fußzeilensymbol            | Ein kleines Symbol, das den Zweck des Fußzeilentexts andeutet.                                                                                                                                                                                                                                                                                                                          | **hFooterIcon** oder **pszFooterIcon**                       |
| Footertext            | Zusätzlicher Text. In den Abbildungen enthält der Text einen Link.                                                                                                                                                                                                                                                                                                                | **pszFooter**                                              |
| Schaltfläche "Allgemein"          | Eine Standardschaltfläche; in den Abbildungen die Schaltfläche OK.                                                                                                                                                                                                                                                                                                                              | **dwCommonButtons**                                        |



 

 

 




