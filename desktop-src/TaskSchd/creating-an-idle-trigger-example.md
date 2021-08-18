---
title: Beispiel zum Erstellen eines Leerlauftriggers
description: Um einen Trigger im Leerlauf zu erstellen, müssen Sie beim Erstellen des Triggers einen Trigger im Leerlauf angeben, und Sie müssen die Leerlaufzeit für den Task festlegen. Informationen zu Leerlaufbedingungen finden Sie unter Bedingungen für den Task-Leerlauf.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac38eb3eb7520fde552f009a718fe188d247e3f9fef943f0f0f79ba6ea85970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139543"
---
# <a name="creating-an-idle-trigger-example"></a>Beispiel zum Erstellen eines Leerlauftriggers

Um einen Trigger im Leerlauf zu erstellen, müssen Sie beim Erstellen des Triggers einen Trigger im Leerlauf angeben, und Sie müssen die Leerlaufzeit für den Task festlegen. Informationen zu Leerlaufbedingungen finden Sie unter [Aufgaben-Leerlaufbedingungen.](task-idle-conditions.md)

Rufen Sie nach dem Erstellen des Triggers im Leerlauf [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) auf, um den neuen Trigger auf dem Datenträger zu speichern.

Im folgenden Verfahren wird beschrieben, wie Sie einen Trigger im Leerlauf für eine bekannte Aufgabe erstellen.

**So erstellen Sie einen Trigger im Leerlauf für eine bekannte Aufgabe**

1.  Rufen [**Sie CoInitialize auf,**](/windows/win32/api/objbase/nf-objbase-coinitialize) um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner zu erhalten. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner ausgeführt wird.)
2.  Rufen [**Sie ITaskScheduler::Activate auf,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Aufgabenobjekts zu erhalten. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testaufgabe" erhält.)
3.  Rufen [**Sie SetIdleWait auf,**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) um zu festlegen, wie lange das System im Leerlauf bleiben muss, bevor der Trigger ausgelöst wird. (Beachten Sie, **dass SetIdleWait** von [**IScheduledWorkItem geerbt wird.)**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
4.  Definieren Sie die [**TASK \_ TRIGGER-Struktur,**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) und rufen [**Sie CreateTrigger auf,**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) um den Trigger im Leerlauf zu erstellen. (Beachten Sie, **dass CreateTrigger** von [**IScheduledWorkItem geerbt wird.)**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)
5.  Speichern Sie die Aufgabe mit dem neuen Trigger im Leerlauf mithilfe von [**IPersistFile::Save auf dem Datenträger.**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) (Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine com-Standardschnittstelle, die von der [**ITask-Schnittstelle unterstützt**](/windows/desktop/api/Mstask/nn-mstask-itask) wird.)
6.  Rufen **Sie ITask::Release auf,** um alle Ressourcen frei zu geben. (Beachten Sie, [**dass Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown-Methode**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ist, die von [**ITask geerbt wird.)**](/windows/desktop/api/Mstask/nn-mstask-itask)



| Ein Codebeispiel für                         | Siehe                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Erstellen eines Triggers im Leerlauf für eine vorhandene Aufgabe | [C/C++-Codebeispiel: Erstellen eines Triggers im Leerlauf](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1.0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 