---
title: Abrufen einer Aufgabenseite (Beispiel)
description: Zum Abrufen einer Aufgabenseite müssen Sie ITask QueryInterface aufrufen, um die iprovidetaskpage-Schnittstelle abzurufen, und dann iprovidetaskpage GetPage aufrufen. Die GetPage-Methode gibt ein Handle für die Seite zurück, die dann zum Anzeigen der angeforderten Seite verwendet werden kann.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- Abrufen der Aufgabenseite Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039157"
---
# <a name="retrieving-a-task-page-example"></a>Abrufen einer Aufgabenseite (Beispiel)

Zum Abrufen einer Aufgabenseite müssen Sie **ITask:: QueryInterface** aufrufen, um die [**iprovidetaskpage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) -Schnittstelle abzurufen, und dann [**iprovidetaskpage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage)aufrufen. Die **GetPage** -Methode gibt ein Handle für die Seite zurück, die dann zum Anzeigen der angeforderten Seite verwendet werden kann.

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem Sie nicht mehr benötigt werden.

 

Im folgenden Verfahren wird das Erstellen eines neuen-Auslösers beschrieben.

**So erstellen Sie einen neuen-Auslösung**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Wenden Sie [**itaskscheduler:: Aktivieren**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) an, um die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle des Task-Objekts abzurufen. (Beachten Sie, dass in diesem Beispiel die Aufgabe "Test Aufgabe" abgerufen wird.)
3.  Rufen Sie **ITask:: QueryInterface** auf, um die [**iprovidetaskpage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) -Schnittstelle und [**iprovidetaskpage:: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) zum Abrufen der Seite abzurufen.
4.  Zeigen Sie mit dem zurückgegebenen Seiten Handle die Seite an.



| Ein Codebeispiel für                                   | Siehe                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Abrufen und Anzeigen der Aufgabenseite einer bekannten Aufgabe | [Abrufen einer Aufgabenseite](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 