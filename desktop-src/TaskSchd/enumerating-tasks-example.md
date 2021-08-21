---
title: Beispiel für das Aufzählen von Aufgaben
description: Zum Aufzählen von Aufgaben müssen Sie ITaskScheduler Enum aufrufen, um ein Enumerationsobjekt zu erstellen. Verwenden Sie dann die IEnumWorkItems-Schnittstelle des Enumerationsobjekts, um die Aufgaben im Ordner Geplante Aufgaben aufzulisten.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf3d5d73d22a1615e819eacfefbf3a7a656bfdb6d83e11ca1dc3cb76c87c7f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118859628"
---
# <a name="enumerating-tasks-example"></a>Beispiel für das Aufzählen von Aufgaben

Um Aufgaben aufzuzählen, müssen Sie [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) aufrufen, um ein [*Enumerationsobjekt*](e.md)zu erstellen. Verwenden Sie dann die [**IEnumWorkItems-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) des Enumerationsobjekts, um die Aufgaben im Ordner Geplante Aufgaben aufzulisten.

Im folgenden Verfahren wird beschrieben, wie die Tasks im Ordner Geplante Aufgaben aufzählt werden.

**So aufzählen Sie die Tasks im Ordner "Geplante Aufgaben"**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) auf, um ein Enumerationsobjekt abzurufen.
3.  Rufen Sie [**IEnumWorkItems::Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) auf, um die Aufgaben abzurufen. (In diesem Beispiel wird versucht, mit jedem Aufruf fünf Aufgaben abzurufen.)
4.  Verarbeiten Sie die zurückgegebenen Aufgaben. (In diesem Beispiel wird einfach der Name der einzelnen Aufgaben auf dem Bildschirm angezeigt.
5.  Freigeben von Ressourcen. Rufen Sie [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um den für Namen verwendeten Arbeitsspeicher freizugeben.



| Ein Codebeispiel für                                                         | Siehe                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Aufzählen aller Aufgaben im Ordner Geplante Aufgaben des lokalen Computers | [C/C++-Codebeispiel: Aufzählen von Aufgaben](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 