---
title: Erstellen einer Aufgabe mithilfe eines NewWorkItem-Beispiels
description: Beim Erstellen einer Aufgabe verwenden Sie zwei schnittstellen Taskplaner ITaskScheduler und ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- Erstellen von Arbeitselementen Taskplaner
- Arbeitselemente Taskplaner , Erstellen von Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d0e0d216c5aaccee6a51cbac939b2b3bfa421338e12d66ffdd3b8cf055862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139583"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Erstellen einer Aufgabe mithilfe eines NewWorkItem-Beispiels

Beim Erstellen einer Aufgabe verwenden Sie zwei Taskplaner Schnittstellen: [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) und [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Sie müssen einen eindeutigen Namen für die Aufgabe, den Klassenbezeichner des Aufgabenobjekts und den Schnittstellenbezeichner **von ITask angeben.** Der Klassenbezeichner und der Schnittstellenbezeichner werden im Codebeispiel nach diesem Thema gezeigt.

> [!Note]  
> Sie können eine Aufgabe auch erstellen, indem Sie [**ITaskScheduler::AddWorkItem aufrufen.**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) Wenn Sie diese Route verwenden, liegt es in Ihrer Verantwortung, eine Instanz des **Task-Objekts** (das die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) unterstützt) zu erstellen und dann die Aufgabe mit dem von Ihnen genannten Namen hinzuzufügen.

 

> [!Note]  
> Standardmäßig kann nur ein Mitglied der Gruppe Administratoren, Sicherungsoperatoren oder Serveroperatoren Aufgaben auf Windows Server 2003 erstellen. Ein Mitglied der Gruppe Administratoren kann die Sicherheitsbeschreibung des Ordners Windows Task ändern, damit \\ andere Personen Aufgaben erstellen können.

 

Der Name, den Sie für den Task angeben, muss innerhalb des Ordners Geplante Aufgaben eindeutig sein. Wenn bereits eine Aufgabe mit dem gleichen Namen vorhanden ist, gibt [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ERROR \_ FILE EXISTS \_ zurück. Wenn Sie diesen Rückgabewert erhalten, sollten Sie einen anderen Namen angeben und versuchen, die Aufgabe erneut zu erstellen.

Im folgenden Verfahren wird beschrieben, wie Sie eine neue Arbeitselementaufgabe erstellen.

**So erstellen Sie eine neue Arbeitselementaufgabe**

1.  Rufen [**Sie CoInitialize auf,**](/windows/win32/api/objbase/nf-objbase-coinitialize) um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner zu erhalten. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner ausgeführt wird.)
2.  Rufen [**Sie ITaskScheduler::NewWorkItem auf,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) um eine neue Aufgabe zu erstellen. (Diese Methode gibt einen Zeiger auf eine [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) zurück.)
3.  Speichern Sie die neue Aufgabe auf dem Datenträger, indem [**Sie IPersistFile::Save aufrufen.**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) (Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine com-Standardschnittstelle, die von der **ITask-Schnittstelle unterstützt** wird.)
4.  Rufen **Sie ITask::Release auf,** um alle Ressourcen frei zu geben. (Beachten Sie, [**dass Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown-Methode**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ist, die von [**ITask geerbt wird.)**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Ein Codebeispiel für  | Siehe                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Erstellen einer einzelnen Aufgabe | [C/C++-Codebeispiel: Erstellen einer Aufgabe mit NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1.0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 