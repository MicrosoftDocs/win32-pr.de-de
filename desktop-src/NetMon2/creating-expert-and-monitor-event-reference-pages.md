---
description: In diesem Abschnitt wird beschrieben, wie Ereignisreferenzseiten (ERPs) geplant, entwickelt und getestet und in einem Experten oder Monitor bereitgestellt werden. Informationen zu ERPs und deren Verwendung mit Netzwerkmonitor finden Sie auf der Ereignisreferenzseite.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Erstellen von Referenzseiten für Experten- und Überwachungsereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5826ab0aaa71461f6b4e56b9330e00c5af6aae26952d84af88c380da6dfe41fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144233"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>Erstellen von Referenzseiten für Experten- und Überwachungsereignisse

In diesem Abschnitt wird beschrieben, wie Ereignisreferenzseiten (ERPs) geplant, entwickelt und getestet und in einem Experten oder Monitor bereitgestellt werden. Informationen zu ERPs und deren Verwendung mit Netzwerkmonitor finden Sie auf der [Ereignisreferenzseite](event-reference-page.md).

Um ein neues ERP zu entwickeln, besteht der erste Schritt darin, die Ereignisse zu bestimmen, die einzelne ERPs für Ihren benutzerdefinierten [Experten](experts.md) oder [Monitor](monitors.md)erfordern. Sie müssen separate ERPs für jedes Ereignis erstellen, das Sie im Netzwerkmonitor Ereignisanzeige anzeigen möchten. Nehmen wir beispielsweise Folgendes an:

-   Sie entwickeln einen Monitor mit dem Namen Game Monitor und Stock Watcher.
-   Der Monitor befindet sich in einer Datei namens Gamemon.dll.
-   Der Monitor generiert zwei Ereignisse: Game Running und My Internet Stock Soars.
-   Sie planen die Entwicklung von zwei ERPs, Gamemon1.htm und Gamemon2.htm.

> [!Note]  
> Es ist nicht erforderlich, eine 1:1-Entsprechung von ERPs zu haben, um Ereignisse oder Expertenereignisse zu überwachen.

 

Nachdem Sie eine Liste eindeutiger ERPs erstellt haben, führen Sie die folgenden Schritte aus, um jedes ERP zu erstellen.

-   [Schreiben Sie das HTML-Quelldokument](writing-an-event-reference-page.md).
-   [Speichern Sie](naming-an-event-reference-page.md) die HTML-Quelldatei, und benennen Sie sie als .htm Datei.
-   [Testen Sie das ERP](testing-an-event-reference-page.md) mit dem abgeschlossenen Experten oder Monitor.

 

 



