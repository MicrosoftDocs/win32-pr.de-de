---
title: Abrufen von Beispielen für Arbeitselementeigenschaften
description: Um die Eigenschaften eines Arbeitselements abzurufen, rufen Sie ITaskScheduler Activate auf, um die Schnittstelle des Arbeitselementobjekts abzurufen, und rufen Sie dann die entsprechende Methode auf, um die gewünschte Aufgabeneigenschaft abzurufen.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- Abrufen von Arbeitselementeigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3519f3f995e4a5c49a58f0c8be590b34a82381bfd534b61bac6ff8aba05de33c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059978"
---
# <a name="retrieving-work-item-property-examples"></a>Abrufen von Beispielen für Arbeitselementeigenschaften

Rufen Sie zum Abrufen der Eigenschaften eines Arbeitselements [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die Schnittstelle des Arbeitselementobjekts abzurufen, und rufen Sie dann die entsprechende Methode auf, um die gewünschte Taskeigenschaft abzurufen. Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.

Die unten auf dieser Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften abgerufen werden, die für alle Arbeitselemente gelten. Informationen zu anderen Eigenschaften, die für Aufgaben eindeutig sind, finden Sie unter [Setting Task Property Examples](setting-task-property-examples.md).

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem sie nicht mehr benötigt werden.

 

Beachten Sie Folgendes: Wenn Sie eine Zeichenfolgeneigenschaft abrufen (z. B. einen Kommentar für ein Arbeitselement), müssen Sie [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) aufrufen, um den für die zurückgegebene Zeichenfolge belegten Arbeitsspeicher freizugeben.

Im folgenden Verfahren wird beschrieben, wie eine Taskeigenschaft abgerufen wird.

**So rufen Sie eine Taskeigenschaft ab**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesen Beispielen wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Taskobjekts abzurufen. (Beachten Sie, dass Aufgaben derzeit der einzige gültige Arbeitselementtyp sind.)
3.  Rufen Sie die entsprechende Methode auf, um die Eigenschaft abzurufen, an der Sie interessiert sind.
4.  Verarbeiten Sie die Eigenschaft nach Bedarf. (In diesen Beispielen wird einfach die -Eigenschaft auf dem Bildschirm gedruckt.)
5.  Wenn die zurückgegebene Eigenschaft eine Zeichenfolge ist, rufen Sie [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den für die zurückgegebene Zeichenfolge belegten Arbeitsspeicher freizugeben.



| Ein Codebeispiel für                                                                        | Siehe                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Abrufen der Kontoinformationen einer bekannten Aufgabe                                           | [C/C++-Codebeispiel: Abrufen von Taskkontoinformationen](c-c-code-example-retrieving-task-account-information.md)       |
| Abrufen der Kommentarzeichenfolge einer bekannten Aufgabe                                                | [C/C++-Codebeispiel: Abrufen eines Aufgabenkommentars](c-c-code-example-retrieving-a-task-comment.md)                           |
| Abrufen des Namens des Erstellers der Aufgabe und Anzeigen auf dem Bildschirm               | [C/C++-Codebeispiel: Abrufen des Aufgabenerstellers](c-c-code-example-retrieving-the-task-creator.md)                       |
| Abrufen des letzten Exitcodes, der von einer bekannten Aufgabe zurückgegeben wurde                                       | [C/C++-Codebeispiel: Abrufen von Task-Exitcode](c-c-code-example-retrieving-task-exit-code.md)                           |
| Abrufen der Leerlaufwartezeit der Aufgabe und Anzeigen auf dem Bildschirm                    | [C/C++-Codebeispiel: Abrufen der Leerlaufwartezeit des Tasks](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Abrufen des Zeitpunkts der letzten Ausführung des Tasks und Anzeigen des Tasks auf dem Bildschirm                    | [C/C++-Codebeispiel: Abrufen des Tasks MostRecentRun Time](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Abrufen des nächsten Zeitpunkts, zu dem die Ausführung des Tasks geplant ist, und Anzeigen dieser Zeit auf dem Bildschirm | [C/C++-Codebeispiel: Abrufen der Aufgabe NextRun Time](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Abrufen der Ausführungszeiten der Aufgabe und Anzeigen auf dem Bildschirm                       | [C/C++-Codebeispiel: Abrufen von Tasklaufzeiten](c-c-code-example-retrieving-task-run-times.md)                           |
| Abrufen des aktuellen Status der Aufgabe und Anzeigen des Tasks auf dem Bildschirm                    | [C/C++-Codebeispiel: Abrufen des Taskstatus](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 