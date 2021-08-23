---
title: Hinzufügen von Arbeitselementen
description: Es gibt zwei Möglichkeiten, dem Ordner Geplante Aufgaben Arbeitselemente hinzuzufügen. Sie können ein neues Arbeitselement im Ordner erstellen oder dem Ordner ein vorhandenes Arbeitselement hinzufügen.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- Arbeitselemente Taskplaner , hinzufügen
- Tasks Taskplaner , hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc964b620a01b0f1114240dcb11f275fa8faffc37e8264d8854cb60191628943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621160"
---
# <a name="adding-work-items"></a>Hinzufügen von Arbeitselementen

Es gibt zwei Möglichkeiten, [*Dem*](w.md) Ordner Geplante [*Aufgaben Arbeitselemente hinzuzufügen.*](s.md) Sie können ein neues Arbeitselement im Ordner erstellen oder dem Ordner ein vorhandenes Arbeitselement hinzufügen.

> [!Note]  
> Derzeit können dem Ordner Geplante Aufgaben nur Taskobjekte hinzugefügt werden. Wenn Sie eine Aufgabe hinzufügen, müssen Sie die Bezeichner für die Aufgabenklasse und die Taskschnittstelle [**ITask kennen.**](/windows/desktop/api/Mstask/nn-mstask-itask)

 

Sie erstellen neue Arbeitselemente, indem Sie die [**ITaskScheduler::NewWorkItem-Methode**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) aufrufen. Diese Methode erstellt ein neues Arbeitselementobjekt unter Verwendung des von Ihnen genannten Namens und fügt das Arbeitselement dem Ordner Geplante Aufgaben hinzu. Wenn Sie ein neues Arbeitselement erstellen, weist der Taskplaner den Arbeitsspeicher zu, der für das neue Objekt erforderlich ist.

Um dem Ordner Geplante Aufgaben vorhandene Arbeitselemente hinzuzufügen, rufen Sie die [**ITaskScheduler::AddWorkItem-Methode**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) auf. Wenn Sie diese Methode aufrufen, müssen Sie das -Objekt erstellen.

Die Namen, die Sie für Arbeitselemente verwenden, müssen innerhalb des Ordners Geplante Aufgaben eindeutig sein. Wenn ein Arbeitselement mit demselben Namen bereits vorhanden ist, wenn Sie entweder die [**ITaskScheduler::NewWorkItem-Methode**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) oder die [**ITaskScheduler::AddWorkItem-Methode**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) aufrufen, gibt die Methode einen **ERROR FILE \_ \_ EXISTS-Fehler** zurück. Weitere Informationen finden Sie unter [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).

 

 




