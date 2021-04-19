---
title: Beispiel für das Abrufen von Beispiel Zeichen folgen
description: Abhängig vom Typ des Objekts, mit dem Sie arbeiten, können Sie die auslöserzeichenfolgen eines bekannten Auslösers mithilfe der ischeduledworkitem-Schnittstelle oder der itaskauslöst-Schnittstelle abrufen.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- Abrufen von Auslöse Zeichen folgen Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341736"
---
# <a name="retrieving-trigger-strings-example"></a>Beispiel für das Abrufen von Beispiel Zeichen folgen

Abhängig vom Typ des Objekts, mit dem Sie arbeiten, können Sie die auslöserzeichenfolgen eines bekannten Auslösers mithilfe der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle oder der [**itaskauslöst**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) -Schnittstelle abrufen.

Verwenden Sie beim Arbeiten mit einem [*Task Objekt*](t.md)die Methoden der [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle, um die auslöserzeichenfolgen einer Arbeitsaufgabe abzurufen.

Wenn Sie mit einem [*taskauslöserobjekt*](t.md)arbeiten, verwenden Sie die-Methoden der [**itaskauslöserschnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , um die auslösende Zeichenfolge des Auslösers abzurufen.

Im folgenden Beispiel wird gezeigt, wie [**ischeduledworkitem:: gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) verwendet wird, um die Zeichen folgen aller mit einer bekannten Aufgabe verknüpften Trigger anzuzeigen.

Im folgenden Verfahren wird beschrieben, wie die auslöserzeichenfolgen einer Aufgabe abgerufen werden.

**So rufen Sie die Auslöse Zeichenfolgen einer Aufgabe ab**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  Aufrufen von **ITask:: gettriggercount** , um herauszufinden, wie viele Trigger einer Aufgabe zugeordnet sind. (Beachten Sie, dass [**gettriggercount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)
4.  Zeigen Sie die auslöserzeichenfolgen an, und rufen Sie **ITask:: gettriggerstring** für jeden der Aufgabe zugeordneten Befehl auf. (Beachten Sie, dass [**gettriggerstring**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) eine [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)
5.  Alle Ressourcen freigeben. Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) zum Freigeben der Trigger-Zeichen folgen und **ITask:: Release** zum Freigeben der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle. (Beachten Sie, dass [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von **ITask** geerbt wird.)



| Ein Codebeispiel für                                                         | Siehe                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Abrufen einer triggerzeichenfolge für alle Trigger, die einer bekannten Aufgabe zugeordnet sind | [Code Beispiel: Abrufen von auslöserzeichenfolgen](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 