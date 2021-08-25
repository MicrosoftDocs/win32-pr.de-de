---
title: Beispiel für das Abrufen einer Aufgabenseite
description: Um eine Aufgabenseite abzurufen, müssen Sie ITask QueryInterface aufrufen, um die IProvideTaskPage-Schnittstelle abzurufen, und dann IProvideTaskPage GetPage aufrufen. Die GetPage-Methode gibt ein Handle für die Seite zurück, das dann zum Anzeigen der angeforderten Seite verwendet werden kann.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- Abrufen der Aufgabenseite Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d619f76b4de416fe2bef9faa679851c613df05e427d6203a6a91936644ad07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872270"
---
# <a name="retrieving-a-task-page-example"></a>Beispiel für das Abrufen einer Aufgabenseite

Um eine Aufgabenseite abzurufen, müssen Sie **ITask::QueryInterface** aufrufen, um die [**IProvideTaskPage-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) abzurufen, und dann [**IProvideTaskPage::GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage)aufrufen. Die **GetPage-Methode** gibt ein Handle für die Seite zurück, das dann zum Anzeigen der angeforderten Seite verwendet werden kann.

> [!Note]  
> Im folgenden Codebeispiel werden alle Schnittstellen freigegeben, nachdem sie nicht mehr benötigt werden.

 

Im folgenden Verfahren wird beschrieben, wie Sie einen neuen Trigger erstellen.

**So erstellen Sie einen neuen Trigger**

1.  Rufen Sie [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) auf, um die COM-Bibliothek zu initialisieren, und [**CoCreateInstance,**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) um ein Taskplaner-Objekt abzurufen. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner Dienst ausgeführt wird.)
2.  Rufen Sie [**ITaskScheduler::Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) auf, um die [**ITask-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-itask) des Taskobjekts abzurufen. (Beachten Sie, dass dieses Beispiel die Aufgabe "Testtask" erhält.)
3.  Rufen Sie **ITask::QueryInterface** auf, um die [**IProvideTaskPage-Schnittstelle**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) abzurufen, und [**IProvideTaskPage::GetPage,**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) um die Seite abzurufen.
4.  Zeigen Sie die Seite mithilfe des zurückgegebenen Seitenhandle an.



| Ein Codebeispiel für                                   | Siehe                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Abrufen und Anzeigen der Seite Aufgabe einer bekannten Aufgabe | [Seite "Abrufen einer Aufgabe"](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[beispiele für Taskplaner 1.0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 