---
title: Abrufen von Aufgaben Eigenschafts Beispielen
description: Um die Eigenschaften einer Aufgabe abzurufen, rufen Sie itaskscheduler aktivieren auf, um die Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende ITask-Methode auf, um die gewünschte Aufgaben Eigenschaft abzurufen.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- Abrufen von Task Eigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2b42bc8044171834b6d99e97c41e3f5c7048ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316047"
---
# <a name="retrieving-task-property-examples"></a>Abrufen von Aufgaben Eigenschafts Beispielen

Rufen Sie zum Abrufen der Eigenschaften einer Aufgabe [**itaskscheduler:: Aktivierungs**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die Schnittstelle des Task-Objekts abzurufen, und rufen Sie dann die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode auf, um die gewünschte Aufgaben Eigenschaft abzurufen. Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die verschiedenen Task Eigenschaften abgerufen werden.

Die unten auf der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften abgerufen werden, die für Aufgaben Objekte eindeutig sind. Weitere Informationen zu anderen [*Arbeits Element*](w.md) Eigenschaften, die auch für Aufgaben gelten, finden Sie unter [Abrufen von Beispielen für Arbeitselemente](retrieving-work-item-property-examples.md).

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.

 

Beachten Sie Folgendes: Wenn Sie eine Zeichen folgen Eigenschaft (z. b. den Anwendungsnamen, Parameter oder das Arbeitsverzeichnis) abrufen, müssen Sie " [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, um den für die zurückgegebenen Zeichenfolge zugeordneten Arbeitsspeicher freizugeben.

Im folgenden Verfahren wird beschrieben, wie eine Task Eigenschaft abgerufen wird.

**So rufen Sie eine Task Eigenschaft ab**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesen Beispielen wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  Rufen Sie die entsprechende [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Methode auf, um die gewünschte Eigenschaft abzurufen.
4.  Verarbeiten Sie die Eigenschaft nach Bedarf. (In diesen Beispielen wird die-Eigenschaft auf dem Bildschirm gedruckt.)
5.  Wenn die zurückgegebene Eigenschaft eine Zeichenfolge ist, können Sie [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) aufrufen, um den für die zurückgegebenen Zeichenfolge belegten Arbeitsspeicher freizugeben.



| Ein Codebeispiel für                                                                                                                           | Siehe                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Abrufen des Namens der Anwendung, die einer bestimmten Aufgabe zugeordnet ist                                                                             | [C/C++-Code Beispiel: Abrufen des Aufgaben Anwendungs namens](c-c-code-example-retrieving-the-task-application-name.md)   |
| Abrufen der maximalen Zeitspanne, die der Task ausgeführt werden kann, und Anzeigen dieser Zahl auf dem Bildschirm                                                 | [C/C++-Code Beispiel: Abrufen der Aufgabe maxruntime](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Abrufen der Parameter Zeichenfolge, die ausgeführt wird, wenn die Aufgabe ausgeführt wird und diese Zeichenfolge auf dem Bildschirm anzeigt                                  | [C/C++-Code Beispiel: Abrufen von Aufgaben Parametern](c-c-code-example-retrieving-task-parameters.md)                       |
| Abrufen der [*Prioritätsstufe*](p.md) der Aufgabe                                                                    | [C/C++-Code Beispiel: Abrufen der Aufgaben Priorität](c-c-code-example-retrieving-task-priority.md)                           |
| Abrufen des [*Arbeitsverzeichnisses*](w.md) einer Aufgabe und Anzeigen des Pfads zum Arbeitsverzeichnis auf dem Bildschirm | [C/C++-Code Beispiel: Abrufen des Aufgaben Arbeitsverzeichnisses](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 