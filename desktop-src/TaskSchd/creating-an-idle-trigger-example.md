---
title: Erstellen eines Beispiels für einen Leerlauf-Timeout
description: Zum Erstellen eines Leerlauf-Auslösers müssen Sie beim Erstellen des Auslösers einen Leerlauf-Auslösers angeben und die Leerlaufzeit für den Task festlegen. Informationen zu Bedingungen im Leerlauf finden Sie Unteraufgaben im Leerlauf.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315926"
---
# <a name="creating-an-idle-trigger-example"></a>Erstellen eines Beispiels für einen Leerlauf-Timeout

Zum Erstellen eines Leerlauf-Auslösers müssen Sie beim Erstellen des Auslösers einen Leerlauf-Auslösers angeben und die Leerlaufzeit für den Task festlegen. Informationen zu Bedingungen im Leerlauf finden Sie unter [Aufgaben im Leerlauf](task-idle-conditions.md).

Nachdem Sie den im Leerlauf befindlichen-Befehl erstellt haben, nennen Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , um den neuen-Befehl auf dem Datenträger

Im folgenden Verfahren wird beschrieben, wie Sie einen Leerlauf-Auslösers für eine bekannte Aufgabe erstellen.

**So erstellen Sie einen Leerlauf-Auslösers für eine bekannte Aufgabe**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  Ruft [**setidlewait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) auf, um festzulegen, wie lange das System im Leerlauf bleiben muss, bevor der Trigger ausgelöst wird. (Beachten Sie, dass "* **tidlewait** " von " [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)" geerbt wird.)
4.  Definieren Sie die [**Task- \_ auslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) , und rufen Sie zum Erstellen des Leerlauf- [**Auslösers**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) den " (Beachten Sie, dass " **kreatetransform** " von " [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)" geerbt wird.)
5.  Speichern Sie die Aufgabe mit dem neuen Leerlauf-Auslösung auf dem Datenträger mithilfe von [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist eine von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützte Standard-COM-Schnittstelle.)
6.  Wenden Sie **ITask:: Release** an, um alle Ressourcen freizugeben. (Beachten Sie, dass [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)



| Ein Codebeispiel für                         | Siehe                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Erstellen eines Leerlauf-Auslösers für eine vorhandene Aufgabe | [C/C++-Code Beispiel: Erstellen eines Leerlauf-Auslösers](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 