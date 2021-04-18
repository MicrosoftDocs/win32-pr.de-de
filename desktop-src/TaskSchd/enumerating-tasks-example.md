---
title: Beispiel für Aufzählung von Aufgaben
description: Zum Auflisten von Tasks müssen Sie die itaskscheduler-Enumeration zum Erstellen eines Enumerationsobjekt aufruft. Verwenden Sie dann die ienumworkitems-Schnittstelle des enumerationsobjeders, um die Aufgaben im Ordner "geplante Aufgaben" aufzuzählen.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338481"
---
# <a name="enumerating-tasks-example"></a>Beispiel für Aufzählung von Aufgaben

Zum Aufzählen von Tasks müssen Sie [**itaskscheduler:: Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) zum Erstellen eines [*Enumerationsobjekt*](e.md)abrufen. Verwenden Sie dann die [**ienumworkitems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) -Schnittstelle des enumerationsobjeders, um die Aufgaben im Ordner "geplante Aufgaben" aufzuzählen.

Im folgenden Verfahren wird beschrieben, wie die Tasks im Ordner "geplante Aufgaben" aufgelistet werden.

**So zählen Sie die Tasks im Ordner "geplante Aufgaben" auf**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Zum Abrufen eines Enumerationsobjekt muss [**itaskscheduler:: Enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) aufgerufen werden.
3.  Rufen Sie [**ienumworkitems:: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) auf, um die Aufgaben abzurufen. (In diesem Beispiel wird versucht, fünf Aufgaben mit jedem-Befehl abzurufen.)
4.  Verarbeiten Sie die zurückgegebenen Aufgaben. (In diesem Beispiel wird einfach der Name der einzelnen Aufgaben auf dem Bildschirm ausgegeben.
5.  Freigeben von Ressourcen. [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) aufrufen, um den für Namen verwendeten Arbeitsspeicher freizugeben.



| Ein Codebeispiel für                                                         | Siehe                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Auflisten aller Aufgaben im Ordner "geplante Aufgaben" des lokalen Computers | [C/C++-Code Beispiel: Auflisten von Tasks](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 