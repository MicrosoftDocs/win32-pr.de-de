---
title: Beispiel für das Beenden einer Aufgabe
description: Sie können eine Aufgabe beenden, während Sie ausgeführt wird, indem Sie ischeduledworkitem beenden aufrufen.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209300"
---
# <a name="terminating-a-task-example"></a>Beispiel für das Beenden einer Aufgabe

Sie können eine Aufgabe beenden, während Sie ausgeführt wird, indem Sie [**ischeduledworkitem:: beenden**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate)aufrufen.

Im folgenden Verfahren wird beschrieben, wie eine Aufgabe beendet wird, wenn Sie ausgeführt wird.

**So beenden Sie einen Task, wenn er ausgeführt wird**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  Aufrufen von **ITask:: GetStatus** , um herauszufinden, ob die Aufgabe ausgeführt wird. (Beachten Sie, dass [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)
4.  Überprüfen Sie den Status des Tasks, und nennen Sie dann **ITask:: beenden** , wenn die Aufgabe ausgeführt wird. (Beachten Sie, dass " [**Beenden**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) " eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)



| Ein Codebeispiel für                | Siehe                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Überprüfen des Status einer bekannten Aufgabe | [C/C++-Code Beispiel: Beenden einer Aufgabe](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 