---
title: Überlegungen zur Programmierung (Taskplaner)
description: Beachten Sie beim Entwickeln von Anwendungen, die den Taskplaner 1,0 verwenden, die folgenden Programmierprobleme. Die Anwendung muss sicherstellen, dass der Taskplaner-Dienst ausgeführt wird, bevor versucht wird, mithilfe der Taskplaner-API Aufrufe durchführen. Wenn Sie Zeichen folgen abrufen, stellen Sie sicher, dass Sie "CoTaskMemFree" aufrufen, um jede Zeichenfolge freizugeben, nachdem Sie nicht mehr benötigt wird. Wenn Sie Arrays von Zeichen folgen abrufen, stellen Sie sicher, dass Sie zuerst jede Zeichenfolge im Array freigeben und dann das Array selbst freigeben. Wenn Sie ein Arbeits Element erstellen oder ändern, einschließlich Triggern, die mit einem Arbeits Element verknüpft sind, stellen Sie sicher, dass Sie IPersistFile speichern, um die Arbeitsaufgabe auf dem Datenträger zu speichern. Nachdem Sie eine der Schnittstellen verwendet haben, die von der Taskplaner-API bereitgestellt werden, stellen Sie sicher, dass Sie die IUnknown-Freigabe zum Freigeben der Schnittstelle IUnknown wird von jedem Taskplaner Objekt unterstützt.
ms.assetid: b9e1806c-acfa-4d44-a371-91bad788648c
keywords:
- Starten Taskplaner
- Überlegungen zur Programmierung Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599652f4a25f3d99020eda0846c41904ee76e5cf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106339109"
---
# <a name="programming-considerations-task-scheduler"></a>Überlegungen zur Programmierung (Taskplaner)

Beachten Sie beim Entwickeln von Anwendungen, die den Taskplaner 1,0 verwenden, die folgenden Programmierprobleme.

-   Die Anwendung muss sicherstellen, dass der Taskplaner-Dienst ausgeführt wird, bevor versucht wird, mithilfe der Taskplaner-API Aufrufe durchführen.
-   Wenn Sie Zeichen folgen abrufen, stellen Sie sicher, dass Sie " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, um jede Zeichenfolge freizugeben, nachdem Sie nicht mehr benötigt wird. Wenn Sie Arrays von Zeichen folgen abrufen, stellen Sie sicher, dass Sie zuerst jede Zeichenfolge im Array freigeben und dann das Array selbst freigeben.
-   Wenn Sie ein Arbeits Element erstellen oder ändern, einschließlich Triggern, die mit einem Arbeits Element verknüpft sind, stellen Sie sicher, dass Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) zum Speichern der Arbeitsaufgabe auf dem Datenträger aufgerufen haben.
-   Nachdem Sie eine der Schnittstellen verwendet haben, die von der Taskplaner-API bereitgestellt werden, stellen Sie sicher, dass Sie [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) zum Freigeben der-Schnittstelle aufruft. [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) wird von jedem Taskplaner Objekt unterstützt.

Der Abschnitt using der Taskplaner-Dokumentation enthält zahlreiche Beispiele, die diese Richtlinien befolgen. In der folgenden Tabelle finden Sie einige dieser Beispiele.

| Beispiel für         | Siehe                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------|
| Freigeben von Zeichen folgen         | [Abrufen von Beispielen für Arbeits Element Eigenschaften](retrieving-work-item-property-examples.md)       |
| Arbeitselemente werden auf dem Datenträger gespeichert | [Festlegen von Beispielen für Arbeits Element Eigenschaften](setting-work-item-property-examples.md)             |
| Freigeben von Schnittstellen      | [Erstellen einer Aufgabe mit NewWorkItem-Beispiel](creating-a-task-using-newworkitem-example.md) |



 

 

 
