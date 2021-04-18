---
title: Festlegen von Aufgaben Eigenschafts Beispielen
description: Um die Eigenschaften einer Aufgabe festzulegen, rufen Sie itaskscheduler aktivieren auf, um die Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende ITask-Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- Festlegen von Task Eigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fcb05031961e38314cbc7cd12c20c1d863f54af
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340278"
---
# <a name="setting-task-property-examples"></a>Festlegen von Aufgaben Eigenschafts Beispielen

Um die Eigenschaften einer Aufgabe festzulegen, rufen Sie [**itaskscheduler:: Aktivierungs**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die-Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode auf, um die gewünschte Aufgaben Eigenschaft festzulegen.

Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften festgelegt werden, die für Aufgaben Objekte eindeutig sind. Informationen zu anderen [*Arbeits Element*](w.md) Eigenschaften, die auch für Aufgaben gelten, finden Sie unter [Festlegen von Beispielen für Arbeits Element](setting-work-item-property-examples.md)Eigenschaften.

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.

 

In den folgenden Beispielen wird das geänderte Task Objekt immer durch einen [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)-Befehl auf dem Datenträger gespeichert. (Die Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine Standard-COM-Schnittstelle, die vom Task-Objekt geerbt wird.)

Im folgenden Verfahren wird beschrieben, wie eine Task Eigenschaft festgelegt wird.

**So legen Sie eine Task Eigenschaft fest**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  Wenden Sie die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode an, um die gewünschte Eigenschaft festzulegen.
4.  Nennen Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , um das geänderte Task Objekt auf dem Datenträger zu speichern.



| Ein Codebeispiel für                                                                                                                                | Siehe                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Festlegen des Namens der Anwendung, die einer bekannten Aufgabe zugeordnet ist                                                                                     | [C/C++-Code Beispiel: Festlegen des Anwendungs namens](c-c-code-example-setting-application-name.md)   |
| Festlegen der maximalen Laufzeit einer bekannten Aufgabe                                                                                                         | [C/C++-Code Beispiel: Festlegen von maxruntime](c-c-code-example-setting-maxruntime.md)               |
| Löschen aller Befehlszeilenparameter, die einer bekannten Aufgabe zugeordnet sind                                                                                    | [C/C++-Code Beispiel: Festlegen von Aufgaben Parametern](c-c-code-example-setting-task-parameters.md)     |
| In diesem Beispiel wird die Priorität einer Testaufgabe festgelegt, und anschließend wird die Aufgabe gespeichert. In diesem Beispiel wird davon ausgegangen, dass die Testaufgabe bereits auf dem lokalen Computer vorhanden ist. | [C/C++-Code Beispiel: Festlegen der Aufgaben Priorität](c-c-code-example-setting-task-priority.md)         |
| Festlegen des [*Arbeitsverzeichnisses*](w.md) einer bekannten Aufgabe                                                                  | [C/C++-Code Beispiel: Festlegen des Arbeitsverzeichnisses](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 