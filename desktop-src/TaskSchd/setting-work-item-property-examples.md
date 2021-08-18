---
title: Beispiele für das Festlegen von Arbeitselementeigenschaft
description: Rufen Sie zum Festlegen der Eigenschaften eines Arbeitselements ITaskScheduler Activate auf, um die Schnittstelle des Arbeitselementobjekts abzurufen, und rufen Sie dann die entsprechende Methode auf, um die für Sie interessierende Aufgabeneigenschaft zu festlegen. Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- Festlegen von Arbeitselementeigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a29ff08c4f9129b8dc9ab749cd6db5807fd0c52449e48b64d5f3b36631fef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402540"
---
# <a name="setting-work-item-property-examples"></a>Beispiele für das Festlegen von Arbeitselementeigenschaft

Rufen Sie zum Festlegen der Eigenschaften eines Arbeitselements [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die Schnittstelle des Arbeitselementobjekts abzurufen, und rufen Sie dann die entsprechende Methode auf, um die für Sie interessierende Aufgabeneigenschaft zu festlegen. Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.

Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften festgelegt werden, die für alle Arbeitselemente gelten. Weitere Eigenschaften, die für Aufgaben eindeutig sind, finden Sie unter [Setting Task Property Examples](setting-task-property-examples.md).

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem sie nicht mehr benötigt werden.

 

In den folgenden Beispielen wird das geänderte Objekt immer durch einen Aufruf von [**IPersistFile::Save auf**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)dem Datenträger gespeichert. (Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine standardmäßige COM-Schnittstelle, die vom Taskobjekt geerbt wird.)

Im folgenden Verfahren wird beschrieben, wie eine Taskeigenschaft festgelegt wird.

**So legen Sie eine Aufgabeneigenschaft fest**

1.  Rufen [**Sie CoInitialize auf,**](/windows/win32/api/objbase/nf-objbase-coinitialize) um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner zu erhalten. (In diesen Beispielen wird davon ausgegangen, Taskplaner dienst ausgeführt wird.)
2.  Rufen [**Sie ITaskScheduler::Activate auf,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Aufgabenobjekts zu erhalten. (Beachten Sie, dass Tasks derzeit der einzige gültige Typ von Arbeitselement sind.)
3.  Rufen Sie die entsprechende [**IScheduledWorkItem-Methode auf,**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) um die Eigenschaft, an der Sie interessiert sind, zu festlegen. Beachten **Sie, dass IScheduledWorkItem-Methoden** von der [**ITask-Schnittstelle geerbt**](/windows/desktop/api/Mstask/nn-mstask-itask) werden.
4.  Rufen [**Sie IPersistFile::Save auf,**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) um das geänderte Aufgabenobjekt auf dem Datenträger zu speichern.



| Ein Codebeispiel für                            | Siehe                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Festlegen der Kontoinformationen für eine bekannte Aufgabe | [C/C++-Codebeispiel: Festlegen von Taskkontoinformationen](c-c-code-example-setting-task-account-information.md) |
| Festlegen des Kommentars einer bekannten Aufgabe              | [C/C++-Codebeispiel: Festlegen des Aufgabenkommentars](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1.0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 