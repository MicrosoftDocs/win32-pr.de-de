---
title: Beispiele für das Abrufen von Aufgabeneigenschaft
description: Rufen Sie zum Abrufen der Eigenschaften einer Aufgabe ITaskScheduler Activate auf, um die Schnittstelle des Aufgabenobjekts abzurufen, und rufen Sie dann die entsprechende ITask-Methode auf, um die task-Eigenschaft abzurufen, an der Sie interessiert sind.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- Abrufen von Aufgabeneigenschaften Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e46554c32d9d30941fd837b91e80e8e20d915b0f1c68a665fd72c8f1624c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002388"
---
# <a name="retrieving-task-property-examples"></a>Beispiele für das Abrufen von Aufgabeneigenschaft

Rufen Sie zum Abrufen der Eigenschaften einer Aufgabe [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die Schnittstelle des Aufgabenobjekts abzurufen, und rufen Sie dann die entsprechende [**ITask-Methode**](/windows/desktop/api/Mstask/nn-mstask-itask) auf, um die task-Eigenschaft abzurufen, an der Sie interessiert sind. Die am unteren Rand der Seite aufgeführten Codebeispiele zeigen, wie die verschiedenen Aufgabeneigenschaften abgerufen werden.

Die am unteren Rand der Seite aufgeführten Codebeispiele zeigen, wie die Eigenschaften abgerufen werden, die für Aufgabenobjekte eindeutig sind. Informationen zu [*anderen Arbeitselementeigenschaften,*](w.md) die auch für Aufgaben gelten, finden Sie unter [Abrufen von Arbeitselementbeispielen.](retrieving-work-item-property-examples.md)

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem sie nicht mehr benötigt werden.

 

Beachten Sie, dass Sie beim Abrufen einer Zeichenfolgeneigenschaft (z. B. Anwendungsname, Parameter oder Arbeitsverzeichnis) [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) aufrufen müssen, um den für die zurückgegebene Zeichenfolge zugeordneten Arbeitsspeicher frei zu geben.

Im folgenden Verfahren wird beschrieben, wie eine Taskeigenschaft abgerufen wird.

**So rufen Sie eine Aufgabeneigenschaft ab**

1.  Rufen [**Sie CoInitialize auf,**](/windows/win32/api/objbase/nf-objbase-coinitialize) um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner zu erhalten. (In diesen Beispielen wird davon ausgegangen, Taskplaner dienst ausgeführt wird.)
2.  Rufen [**Sie ITaskScheduler::Activate auf,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Aufgabenobjekts zu erhalten. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testaufgabe" erhält.)
3.  Rufen Sie die entsprechende [**ITask-Methode**](/windows/desktop/api/Mstask/nn-mstask-itask) auf, um die Eigenschaft abzurufen, an der Sie interessiert sind.
4.  Verarbeiten Sie die Eigenschaft nach Bedarf. (In diesen Beispielen wird die -Eigenschaft auf dem Bildschirm gedruckt.)
5.  Wenn die zurückgegebene Eigenschaft eine Zeichenfolge ist, rufen [Sie CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den für die zurückgegebene Zeichenfolge zugeordneten Arbeitsspeicher frei zu geben.



| Ein Codebeispiel für                                                                                                                           | Siehe                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Abrufen des Namens der Anwendung, die einer bestimmten Aufgabe zugeordnet ist                                                                             | [C/C++-Codebeispiel: Abrufen des Taskanwendungsnamens](c-c-code-example-retrieving-the-task-application-name.md)   |
| Abrufen der maximalen Zeitdauer, die der Task ausgeführt werden kann, und Anzeigen dieser Zahl auf dem Bildschirm                                                 | [C/C++-Codebeispiel: Abrufen der Aufgabe "MaxRunTime"](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Abrufen der Parameterzeichenfolge, die ausgeführt wird, wenn der Task ausgeführt wird, und Anzeigen dieser Zeichenfolge auf dem Bildschirm                                  | [C/C++-Codebeispiel: Abrufen von Taskparametern](c-c-code-example-retrieving-task-parameters.md)                       |
| Abrufen der [*Prioritätsebene*](p.md) der Aufgabe                                                                    | [C/C++-Codebeispiel: Abrufen der Aufgabenpriorität](c-c-code-example-retrieving-task-priority.md)                           |
| Abrufen des [*Arbeitsverzeichnisses*](w.md) einer Aufgabe und Anzeigen des Pfads zum Arbeitsverzeichnis auf dem Bildschirm | [C/C++-Codebeispiel: Abrufen des Taskarbeitsverzeichnisses](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1.0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 