---
title: Erstellen eines neuen Triggers
description: Zum Erstellen eines Triggers müssen Sie drei Schnittstellen verwenden.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0111fe8c45fdac5618407500b2168bf09c4ec01c5d68e78342f14d6bf103ff78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100440"
---
# <a name="creating-a-new-trigger"></a>Erstellen eines neuen Triggers

Zum Erstellen eines Triggers müssen Sie drei Schnittstellen verwenden. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) stellt die [**IScheduledWorkItem::CreateTrigger-Methode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) zum Erstellen des Triggerobjekts bereit, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) stellt die [**ITaskTrigger::SetTrigger-Methode**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) zum Festlegen der Kriterien für den Trigger bereit, und die COM-Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) stellt eine **Save-Methode** zum Speichern des neuen Triggers auf dem Datenträger bereit.

Im folgenden Verfahren wird beschrieben, wie Sie einen neuen Trigger erstellen.

**So erstellen Sie einen neuen Trigger**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Taskobjekts abzurufen. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testtask" erhält.)
3.  Rufen [**Sie CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) auf, um ein Triggerobjekt zu erstellen. (Beachten Sie, dass [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) von [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)geerbt wird.)
4.  Definieren Sie eine [**TASK \_ TRIGGER-Struktur.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Beachten Sie, dass die Mitglieder wBeginDay, wBeginMonth und wBeginYear von **TASK \_ TRIGGER** auf einen gültigen Tag, Monat und Jahr festgelegt werden müssen.
5.  Rufen Sie [**ITaskTrigger::SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) auf, um die Triggerkriterien festzulegen.
6.  Speichern Sie die Aufgabe mit dem neuen Trigger mithilfe von [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)auf dem Datenträger. (Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine com-Standardschnittstelle, die von der [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) unterstützt wird.)
7.  Rufen Sie [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf, um alle Ressourcen freizugeben. (Beachten Sie, dass **Release** eine von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbte [**IUnknown-Methode**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ist.)



| Ein Codebeispiel für                       | Siehe                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Erstellen eines neuen Triggers für eine vorhandene Aufgabe | [C/C++-Codebeispiel: Erstellen eines Aufgabentriggers](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 