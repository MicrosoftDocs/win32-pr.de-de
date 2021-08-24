---
title: Festlegen von Aufgabeneigenschaftenbeispielen
description: Um die Eigenschaften einer Aufgabe festzulegen, rufen Sie ITaskScheduler Activate auf, um die Schnittstelle des Taskobjekts abzurufen, und rufen Sie dann die entsprechende ITask-Methode auf, um die gewünschte Taskeigenschaft festzulegen.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- Festlegen von Taskeigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deac57ac28a16108eb886cc56cf697cd768ca7d2e351c4517728c2972be8582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681630"
---
# <a name="setting-task-property-examples"></a>Festlegen von Aufgabeneigenschaftenbeispielen

Um die Eigenschaften einer Aufgabe festzulegen, rufen [**Sie ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die Schnittstelle des Taskobjekts abzurufen, und rufen Sie dann die entsprechende [**ITask-Methode**](/windows/desktop/api/Mstask/nn-mstask-itask) auf, um die gewünschte Taskeigenschaft festzulegen.

Die am unteren Rand der Seite aufgeführten Codebeispiele zeigen, wie Sie die Eigenschaften festlegen, die für Aufgabenobjekte eindeutig sind. Informationen zu anderen [*Arbeitselementeigenschaften,*](w.md) die auch für Aufgaben gelten, finden Sie unter [Setting Work Item Property Examples](setting-work-item-property-examples.md).

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem sie nicht mehr benötigt werden.

 

In den folgenden Beispielen wird das geänderte Taskobjekt immer durch einen Aufruf von [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)auf dem Datenträger gespeichert. (Die [**IPersistFile-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine COM-Standardschnittstelle, die vom Taskobjekt geerbt wird.)

Im folgenden Verfahren wird beschrieben, wie eine Taskeigenschaft festgelegt wird.

**So legen Sie eine Taskeigenschaft fest**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesen Beispielen wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Taskobjekts abzurufen. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testtask" erhält.)
3.  Rufen Sie die entsprechende [**ITask-Methode**](/windows/desktop/api/Mstask/nn-mstask-itask) auf, um die gewünschte Eigenschaft festzulegen.
4.  Rufen Sie [**IPersistFile::Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) auf, um das geänderte Taskobjekt auf dem Datenträger zu speichern.



| Ein Codebeispiel für                                                                                                                                | Siehe                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Festlegen des Namens der Anwendung, die einer bekannten Aufgabe zugeordnet ist                                                                                     | [C/C++-Codebeispiel: Festlegen des Anwendungsnamens](c-c-code-example-setting-application-name.md)   |
| Festlegen der maximalen Laufzeit einer bekannten Aufgabe                                                                                                         | [C/C++-Codebeispiel: Festlegen von MaxRunTime](c-c-code-example-setting-maxruntime.md)               |
| Löschen aller Befehlszeilenparameter, die einer bekannten Aufgabe zugeordnet sind                                                                                    | [C/C++-Codebeispiel: Festlegen von Taskparametern](c-c-code-example-setting-task-parameters.md)     |
| In diesem Beispiel wird die Priorität eines Testtasks festgelegt und anschließend gespeichert. In diesem Beispiel wird davon ausgegangen, dass der Testtask bereits auf dem lokalen Computer vorhanden ist. | [C/C++-Codebeispiel: Festlegen der Taskpriorität](c-c-code-example-setting-task-priority.md)         |
| Festlegen des [*Arbeitsverzeichnisses*](w.md) einer bekannten Aufgabe                                                                  | [C/C++-Codebeispiel: Festlegen des Arbeitsverzeichnisses](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 