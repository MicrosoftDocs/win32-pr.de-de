---
title: Beispiel für das Starten einer Aufgabe
description: Um eine Aufgabe zu starten, können Sie die Run-Methode der ITask-Schnittstelle aufzurufen. Run ist eine asynchrone Methode, die versucht, die Aufgabe auszuführen, und gibt zurück, sobald die Aufgabe gestartet wurde. Der Taskplaner-Dienst muss ausgeführt werden, damit diese Methode erfolgreich ausgeführt wird.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341953"
---
# <a name="starting-a-task-example"></a>Beispiel für das Starten einer Aufgabe

Um eine Aufgabe zu starten, können Sie die [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) -Methode der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle aufzurufen. **Run** ist eine asynchrone Methode, die versucht, die Aufgabe auszuführen, und gibt zurück, sobald die Aufgabe gestartet wurde. Der Taskplaner-Dienst muss ausgeführt werden, damit diese Methode erfolgreich ausgeführt wird.

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe gestartet wird.

**So starten Sie eine Aufgabe**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  [**Führen**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) Sie aus, um die Aufgabe zu starten. Beachten Sie, dass diese Methode von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle geerbt wird.
4.  Fortsetzen der Verarbeitung nach Bedarf.
5.  Wenden Sie **ITask:: Release** an, um Ressourcen frei [**zugeben und die Initialisierung von**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) com aufzuheben. In diesem Beispiel wird Release aufgerufen, um den Zeiger auf die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle frei [**zugeben**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . (Beachten Sie, dass **Release** eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von **ITask** geerbt wird.)



| Ein Codebeispiel für    | Siehe                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Ausführen einer vorhandenen Aufgabe | [C/C++-Code Beispiel: Starten einer Aufgabe](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 