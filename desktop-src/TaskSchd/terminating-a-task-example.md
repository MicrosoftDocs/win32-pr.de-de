---
title: Beispiel zum Beenden einer Aufgabe
description: Sie können eine Aufgabe beenden, während sie ausgeführt wird, indem Sie IScheduledWorkItem Terminate aufrufen.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2705687b5383589c297348b1b5efa805b8ab407aeaef1c8c1213b1f9f6b0e894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118354772"
---
# <a name="terminating-a-task-example"></a>Beispiel zum Beenden einer Aufgabe

Sie können eine Aufgabe beenden, während sie ausgeführt wird, indem [**Sie IScheduledWorkItem::Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)aufrufen.

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe beendet wird, wenn sie ausgeführt wird.

**So beenden Sie eine Aufgabe, wenn sie ausgeführt wird**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Taskobjekts abzurufen. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testtask" erhält.)
3.  Rufen **Sie ITask::GetStatus** auf, um herauszufinden, ob die Aufgabe ausgeführt wird. (Beachten [**Sie,**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) dass GetStatus eine [**IScheduledWorkItem-Methode**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)
4.  Überprüfen Sie den Status der Aufgabe, und rufen Sie dann **ITask::Terminate** auf, wenn der Task ausgeführt wird. (Beachten Sie, dass [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) eine von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbte [**IScheduledWorkItem-Methode**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ist.)



| Ein Codebeispiel für                | Siehe                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Überprüfen des Status einer bekannten Aufgabe | [C/C++-Codebeispiel: Beenden einer Aufgabe](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 