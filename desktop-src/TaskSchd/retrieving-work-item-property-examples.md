---
title: Abrufen von Beispielen für Arbeits Element Eigenschaften
description: Um die Eigenschaften eines Arbeits Elements abzurufen, rufen Sie itaskscheduler aktivieren auf, um die Schnittstelle des Arbeits Element Objekts abzurufen, und rufen Sie dann die entsprechende Methode auf, um die gewünschte Aufgaben Eigenschaft abzurufen.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- Abrufen von Arbeits Element Eigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a51c623301a4a3b53369713abe95ea1dafba80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390591"
---
# <a name="retrieving-work-item-property-examples"></a>Abrufen von Beispielen für Arbeits Element Eigenschaften

Rufen Sie zum Abrufen der Eigenschaften einer Arbeitsaufgabe [**itaskscheduler:: Aktivierungs**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die-Schnittstelle des Arbeits Element Objekts abzurufen, und rufen Sie dann die entsprechende-Methode auf, um die gewünschte Aufgaben Eigenschaft abzurufen. Derzeit sind die einzigen gültigen Arbeitselemente Aufgaben.

Die unten auf dieser Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften abgerufen werden, die für alle Arbeitsaufgaben gelten. Informationen zu anderen Eigenschaften, die für aufgabenspezifisch sind, finden Sie unter [Setting Task Property examples](setting-task-property-examples.md).

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.

 

Beachten Sie Folgendes: Wenn Sie eine Zeichen folgen Eigenschaft (z. b. einen Kommentar für eine Arbeitsaufgabe) abrufen, müssen Sie " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, um den für die zurückgegebenen Zeichenfolge zugeordneten Arbeitsspeicher freizugeben.

Im folgenden Verfahren wird beschrieben, wie eine Task Eigenschaft abgerufen wird.

**So rufen Sie eine Task Eigenschaft ab**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass Aufgaben derzeit der einzige gültige Typ von Arbeits Element sind.)
3.  Rufen Sie die entsprechende Methode auf, um die gewünschte Eigenschaft abzurufen.
4.  Verarbeiten Sie die Eigenschaft nach Bedarf. (In diesen Beispielen wird die-Eigenschaft einfach auf dem Bildschirm gedruckt.)
5.  Wenn die zurückgegebene Eigenschaft eine Zeichenfolge ist, können Sie [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) aufrufen, um den für die zurückgegebenen Zeichenfolge belegten Arbeitsspeicher freizugeben.



| Ein Codebeispiel für                                                                        | Siehe                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Abrufen der Kontoinformationen einer bekannten Aufgabe                                           | [C/C++-Code Beispiel: Abrufen von Aufgaben Kontoinformationen](c-c-code-example-retrieving-task-account-information.md)       |
| Abrufen der Kommentar Zeichenfolge einer bekannten Aufgabe                                                | [C/C++-Code Beispiel: Abrufen eines Aufgaben Kommentars](c-c-code-example-retrieving-a-task-comment.md)                           |
| Abrufen des Namens des Erstellers der Aufgabe und Anzeigen der Aufgabe auf dem Bildschirm               | [C/C++-Code Beispiel: Abrufen des Aufgaben Erstellers](c-c-code-example-retrieving-the-task-creator.md)                       |
| Abrufen des letzten von einer bekannten Aufgabe zurückgegebenen Exitcodes                                       | [C/C++-Codebeispiel: Abrufen von taskexitcode](c-c-code-example-retrieving-task-exit-code.md)                           |
| Abrufen der Leerlaufzeit der Aufgabe und Anzeigen der Wartezeit auf dem Bildschirm                    | [C/C++-Code Beispiel: Abrufen von Aufgaben im Leerlauf: Wartezeit](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Abrufen der Uhrzeit, zu der die Aufgabe zuletzt ausgeführt wurde und auf dem Bildschirm angezeigt wird                    | [C/C++-Code Beispiel: Abrufen der Aufgabe "mustrecentrun"](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Abrufen des nächsten Zeitplans für die Ausführung der Aufgabe und Anzeigen dieser Uhrzeit auf dem Bildschirm | [C/C++-Code Beispiel: Abrufen der Task-nextrun-Zeit](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Abrufen der Ausführungszeiten der Aufgabe und Anzeigen der Ausführungszeiten auf dem Bildschirm                       | [C/C++-Code Beispiel: Abrufen von Task Ausführungszeiten](c-c-code-example-retrieving-task-run-times.md)                           |
| Abrufen des aktuellen Status der Aufgabe und Anzeigen der Aufgabe auf dem Bildschirm                    | [C/C++-Code Beispiel: Abrufen des Task Status](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 