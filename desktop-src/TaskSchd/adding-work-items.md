---
title: Hinzufügen von Arbeits Elementen
description: Es gibt zwei Möglichkeiten, dem geplanten tasksordner Arbeitselemente hinzuzufügen. Sie können ein neues Arbeits Element innerhalb des Ordners erstellen, oder Sie können dem Ordner ein vorhandenes Arbeits Element hinzufügen.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- Arbeitselemente Taskplaner, hinzufügen
- Aufgaben Taskplaner, hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338598"
---
# <a name="adding-work-items"></a>Hinzufügen von Arbeits Elementen

Es gibt zwei Möglichkeiten, dem [*geplanten tasksordner*](s.md) [*Arbeitselemente*](w.md) hinzuzufügen. Sie können ein neues Arbeits Element innerhalb des Ordners erstellen, oder Sie können dem Ordner ein vorhandenes Arbeits Element hinzufügen.

> [!Note]  
> Derzeit können dem Ordner "geplante Aufgaben" nur Aufgaben Objekte hinzugefügt werden. Wenn Sie eine Aufgabe hinzufügen, müssen Sie die Bezeichner für die Aufgaben Klasse und die Aufgaben Schnittstelle [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)kennen.

 

Sie erstellen neue Arbeitselemente, indem Sie die [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) -Methode aufrufen. Diese Methode erstellt ein neues Arbeits Element Objekt mit dem von Ihnen angegebenen Namen und fügt das Arbeits Element dem Ordner "geplante Aufgaben" hinzu. Wenn Sie ein neues Arbeits Element erstellen, ordnet der Taskplaner den für das neue-Objekt erforderlichen Arbeitsspeicher zu.

Um dem Ordner "geplante Aufgaben" vorhandene Arbeitselemente hinzuzufügen, müssen Sie die [**itaskscheduler:: addworkitem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) -Methode aufzurufen. Wenn Sie diese Methode aufgerufen haben, müssen Sie das-Objekt erstellen.

Die Namen, die Sie für Arbeitselemente angeben, müssen innerhalb des Ordners für geplante Aufgaben eindeutig sein. Wenn eine Arbeitsaufgabe mit dem gleichen Namen bereits vorhanden ist, wenn Sie entweder die [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) -Methode oder die [**itaskscheduler:: addworkitem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) -Methode aufruft, gibt die Methode eine **Fehler Datei "ist \_ \_ vorhanden** " zurück. Weitere Informationen finden Sie unter [Erstellen einer Aufgabe mit NewWorkItem-Beispiel](creating-a-task-using-newworkitem-example.md).

 

 




