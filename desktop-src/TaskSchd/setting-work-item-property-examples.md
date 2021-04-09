---
title: Festlegen von Beispielen für Arbeits Element Eigenschaften
description: Um die Eigenschaften eines Arbeits Elements festzulegen, rufen Sie itaskscheduler aktivieren auf, um die Schnittstelle des Arbeits Element Objekts abzurufen, und rufen Sie dann die entsprechende Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen. Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- Festlegen von Arbeits Element Eigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948956"
---
# <a name="setting-work-item-property-examples"></a>Festlegen von Beispielen für Arbeits Element Eigenschaften

Um die Eigenschaften eines Arbeits Elements festzulegen, rufen Sie [**itaskscheduler:: Aktivierungs**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die-Schnittstelle des Arbeits Element Objekts abzurufen, und rufen Sie dann die entsprechende-Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen. Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.

Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften festgelegt werden, die für alle Arbeitsaufgaben gelten. Informationen zu anderen Eigenschaften, die für aufgabenspezifisch sind, finden Sie unter [Setting Task Property examples](setting-task-property-examples.md).

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.

 

In den folgenden Beispielen wird das geänderte Objekt immer durch einen [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)-Befehl auf dem Datenträger gespeichert. (Die Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine Standard-COM-Schnittstelle, die vom Task-Objekt geerbt wird.)

Im folgenden Verfahren wird beschrieben, wie eine Task Eigenschaft festgelegt wird.

**So legen Sie eine Task Eigenschaft fest**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass Aufgaben derzeit der einzige gültige Typ von Arbeits Element sind.)
3.  Wenden Sie die entsprechende [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode an, um die Eigenschaft festzulegen, an der Sie interessiert sind. Beachten Sie, dass die **ischeduledworkitem** -Methoden von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle geerbt werden.
4.  Nennen Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , um das geänderte Task Objekt auf dem Datenträger zu speichern.



| Ein Codebeispiel für                            | Siehe                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Festlegen der Kontoinformationen für eine bekannte Aufgabe | [C/C++-Code Beispiel: Festlegen von Informationen zum Task Konto](c-c-code-example-setting-task-account-information.md) |
| Festlegen eines Kommentars für eine bekannte Aufgabe              | [C/C++-Code Beispiel: Festlegen des Aufgaben Kommentars](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 