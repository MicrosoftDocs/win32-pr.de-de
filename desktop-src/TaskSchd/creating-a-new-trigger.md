---
title: Erstellen eines neuen-Auslösers
description: Zum Erstellen eines-Auslösers müssen Sie drei Schnittstellen verwenden.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390679"
---
# <a name="creating-a-new-trigger"></a>Erstellen eines neuen-Auslösers

Zum Erstellen eines-Auslösers müssen Sie drei Schnittstellen verwenden. [**Ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) stellt die [**ischeduledworkitem:: up-auslösermethode**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) zum Erstellen des-auslöserobjekts bereit. [**itaskausgelöst**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) stellt die [**itaskausgelöst:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) -Methode zum Festlegen der Kriterien für den-Befehl bereit, und die COM-Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) bietet eine **Save** -Methode zum Speichern des neuen-Auslösers

Im folgenden Verfahren wird das Erstellen eines neuen-Auslösers beschrieben.

**So erstellen Sie einen neuen-Auslösung**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  Rufen [**Sie**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) zum Erstellen eines-auslöserobjekts "up" auf. (Beachten Sie, dass " [**kreatetransform**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) " von " [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)" geerbt wird.)
4.  Definieren Sie eine [**Aufgaben \_ auslöserstruktur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Beachten Sie, dass die Member "wbeginday", "wbeginmonth" und "wbeginyear" des **Task- \_ Auslösers** auf einen gültigen Tag, Monat und Jahr festgelegt werden müssen.
5.  Wenden Sie [**itaskausgelöst:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) an, um die Auslöserkriterien festzulegen.
6.  Speichern Sie die Aufgabe mit dem neuen-Vorgang auf dem Datenträger mithilfe von [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist eine von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützte Standard-COM-Schnittstelle.)
7.  Ruft die [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf, um alle Ressourcen freizugeben. (Beachten Sie, dass **Release** eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)



| Ein Codebeispiel für                       | Siehe                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Erstellen eines neuen-Auslösers für eine vorhandene Aufgabe | [C/C++-Code Beispiel: Erstellen eines Aufgaben Auslösers](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 