---
title: Beispiel zum Starten einer Aufgabe
description: Um eine Aufgabe zu starten, rufen Sie die Run-Methode der ITask-Schnittstelle auf. Run ist eine asynchrone Methode, die versucht, die Aufgabe auszuführen, und die zurückgibt, sobald der Task gestartet wurde. Der Taskplaner Dienst muss ausgeführt werden, damit diese Methode erfolgreich ausgeführt werden kann.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4176bf793e72acd3930d6e1e5cbc3d73e91c1d558e342a5a9804aa8f87526cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139333"
---
# <a name="starting-a-task-example"></a>Beispiel zum Starten einer Aufgabe

Um eine Aufgabe zu starten, rufen Sie die [**Run-Methode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) der [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) auf. **Run** ist eine asynchrone Methode, die versucht, die Aufgabe auszuführen, und die zurückgibt, sobald der Task gestartet wurde. Der Taskplaner Dienst muss ausgeführt werden, damit diese Methode erfolgreich ausgeführt werden kann.

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe gestartet wird.

**So starten Sie eine Aufgabe**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Taskobjekts abzurufen. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testtask" erhält.)
3.  Rufen [**Sie Ausführen**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) auf, um die Aufgabe zu starten. Beachten Sie, dass diese Methode von der [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) geerbt wird.
4.  Setzen Sie die Verarbeitung nach Bedarf fort.
5.  Rufen Sie **ITask::Release** auf, um Ressourcen freizugeben, und [**CoUninitialize,**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) um com zu initialisieren. Dieses Beispiel ruft [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf, um den Zeiger auf die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) freizugeben. (Beachten Sie, dass **Release** eine von **ITask** geerbte [**IUnknown-Methode**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ist.)



| Ein Codebeispiel für    | Siehe                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Ausführen einer vorhandenen Aufgabe | [C/C++-Codebeispiel: Starten einer Aufgabe](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 