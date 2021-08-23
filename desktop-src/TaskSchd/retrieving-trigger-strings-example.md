---
title: Beispiel zum Abrufen von Triggerzeichenfolgen
description: Sie können die Triggerzeichenfolgen eines bekannten Triggers mithilfe der IScheduledWorkItem- oder ITaskTrigger-Schnittstelle abrufen, je nachdem, mit welchem Objekttyp Sie arbeiten.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- Abrufen von Triggerzeichenfolgen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a05f95f19aaa68927059c87f7a73f162266454137fbe088923b25dce7ed3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002378"
---
# <a name="retrieving-trigger-strings-example"></a>Beispiel zum Abrufen von Triggerzeichenfolgen

Sie können die Triggerzeichenfolgen eines bekannten Triggers mithilfe der [**IScheduledWorkItem-**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) oder [**ITaskTrigger-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) abrufen, je nachdem, mit welchem Objekttyp Sie arbeiten.

Wenn Sie mit einem [*Aufgabenobjekt*](t.md)arbeiten, verwenden Sie die Methoden der [**IScheduledWorkItem-Schnittstelle,**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) um die Triggerzeichenfolgen eines Arbeitselements abzurufen.

Wenn Sie mit einem [*Aufgabentriggerobjekt*](t.md)arbeiten, verwenden Sie die Methoden der [**ITaskTrigger-Schnittstelle,**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) um die Triggerzeichenfolge des Triggers abzurufen.

Das folgende Beispiel zeigt, wie [**IScheduledWorkItem::GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) verwendet wird, um die Zeichenfolgen aller Trigger anzuzeigen, die einer bekannten Aufgabe zugeordnet sind.

Im folgenden Verfahren wird beschrieben, wie die Triggerzeichenfolgen einer Aufgabe abgerufen werden.

**So rufen Sie die Triggerzeichenfolgen einer Aufgabe ab**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Taskobjekts abzurufen. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testtask" erhält.)
3.  Rufen Sie **ITask::GetTriggerCount** auf, um herauszufinden, wie viele Trigger einer Aufgabe zugeordnet sind. (Beachten [**Sie, dass GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) eine [**IScheduledWorkItem-Methode**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)
4.  Zeigen Sie die Triggerzeichenfolgen an, und rufen **Sie ITask::GetTriggerString** für jeden Trigger auf, der der Aufgabe zugeordnet ist. (Beachten [**Sie, dass GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) eine von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbte [**IScheduledWorkItem-Methode**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ist.)
5.  Geben Sie alle Ressourcen frei. Rufen Sie [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um die Triggerzeichenfolgen freizugeben, und **ITask::Release,** um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) freizugeben. (Beachten Sie, dass [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine von **ITask** geerbte [**IUnknown-Methode**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ist.)



| Ein Codebeispiel für                                                         | Siehe                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Abrufen einer Triggerzeichenfolge für alle Trigger, die einer bekannten Aufgabe zugeordnet sind | [Codebeispiel: Abrufen von Triggerzeichenfolgen](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 