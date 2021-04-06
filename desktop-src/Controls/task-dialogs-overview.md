---
title: Informationen über Aufgaben Dialoge
description: Bei einem Aufgabendialogfeld handelt es sich um ein Dialogfeld zum Anzeigen von Informationen und zum Entgegennehmen einfacher Eingaben des Benutzers.
ms.assetid: vs|controls|~\controls\toolbar\taskdialogsoverview.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb5cafa452a4ed653c404d053e888c6de644236
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947555"
---
# <a name="about-task-dialogs"></a>Informationen über Aufgaben Dialoge

Bei einem Aufgabendialogfeld handelt es sich um ein Dialogfeld zum Anzeigen von Informationen und zum Entgegennehmen einfacher Eingaben des Benutzers. Wie ein Meldungs Feld wird es gemäß den von Ihnen festgelegten Parametern vom Betriebssystem formatiert. Ein Aufgaben Dialogfeld weist jedoch viele weitere Funktionen auf als ein Meldungs Feld.

> [!Note]  
> Aufgaben Dialogfelder erfordern das STA-Modell (Single Thread-Apartment).

 

## <a name="parts-of-a-task-dialog"></a>Teile eines Aufgaben Dialogfelds

Ein Aufgaben Dialogfeld besteht aus mehreren Elementen, von denen die meisten optional sind. Die folgende Abbildung zeigt die verschiedenen Teile eines Aufgaben Dialogfelds.

![Screenshot eines Fensters, das verschiedene Schaltflächen anzeigt, einschließlich eines neben dem reduzierten Steuerelement Text](images/taskdialog.jpg)

In der folgenden Abbildung hat der Benutzer auf die Schaltfläche neben dem reduzierten Steuerelement Text geklickt, wodurch alternativer Text dort und in der Fußzeile angezeigt wird.

![Screenshot des vorherigen Fensters, aber mit zwei Zeilen mit erweitertem Steuerelement Text](images/taskdialogexpand.jpg)

Die Abbildungen zeigen die folgenden Teile:



| Teil                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          | TASKDIALOGCONFIG-Member                                    |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Fenstertitel           | Beschriftung des Fensters.                                                                                                                                                                                                                                                                                                                                                               | **pszwindowtitle**                                         |
| Hauptsymbol              | Ein großes Symbol, das den Zweck des Aufgaben Dialogfelds angibt.                                                                                                                                                                                                                                                                                                                          | **hmainicon** oder **pszmainicon**                           |
| Main-Anweisung       | Prinzipal Text.                                                                                                                                                                                                                                                                                                                                                                      | **pszmaininstruction**                                     |
| Inhalt                | Zusätzlicher Text.                                                                                                                                                                                                                                                                                                                                                                          | **pszcontent**                                             |
| Statusleiste           | Eine animierte Leiste, die den Fortschritt einer Aufgabe anzeigt.                                                                                                                                                                                                                                                                                                                                | **dwFlags**                                                |
| Optionsfelder          | Anwendungs definierte Optionen für den Benutzer.                                                                                                                                                                                                                                                                                                                                            | **"pradiobuttons"**                                          |
| Benutzerdefinierte Schaltfläche          | Eine Schaltfläche, die nicht zu den allgemeinen Schaltflächen gehört. Dies kann entweder eine normale Schaltfläche oder, wie in der Abbildung gezeigt, ein Befehls Link mit bis zu zwei Textzeilen sein.                                                                                                                                                                                                                    | **pbuttons**                                               |
| Schaltfläche zum erweitern/reduzieren | Eine Schaltfläche, die verwendet werden kann, um zwischen dem Anwendungs definierten reduzierten Steuerelement Text (z. b. "Weitere Details anzeigen") und dem erweiterten Steuerelement Text zu wechseln, der sich in zwei oder mehr Zeilen befinden kann. Wenn der Steuerelement Text erweitert ist, wird der zusätzliche Text in **pszexpandecodinformation** auch nach dem Inhalts Text oder (wie in der zweiten Abbildung gezeigt) in der Fußzeile angezeigt. | **pszredusedcontroltext** und **pszexpandecodcontroltext** |
| Überprüfungs Kontrollkästchen | Ein Kontrollkästchen, das von Anwendungs definiertem Text begleitet wird, für einfache Optionen, wie z. b. "dieses Dialogfeld nicht mehr anzeigen".                                                                                                                                                                                                                                                                     | **pszverificationtext**                                    |
| Footersymbol            | Ein kleines Symbol, das den Zweck des Footertexts angibt.                                                                                                                                                                                                                                                                                                                          | **hfootericon** oder **pszfootericon**                       |
| Footertext            | Zusätzlicher Text. In den Abbildungen enthält der Text einen Hyperlink.                                                                                                                                                                                                                                                                                                                | **pszfooter**                                              |
| Allgemeine Schaltfläche          | Eine Standard Schaltfläche. in den Abbildungen die Schaltfläche OK.                                                                                                                                                                                                                                                                                                                              | **dwcommonbuttons**                                        |



 

 

 




