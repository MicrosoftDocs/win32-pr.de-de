---
description: In diesem Abschnitt wird beschrieben, wie Sie Ereignis Referenzseiten (Erps) planen, entwickeln und testen und wie Sie Sie in einem Experten oder Monitor bereitstellen. Weitere Informationen zu Erps und deren Verwendung mit Netzwerkmonitor finden Sie auf der Seite mit der Ereignis Referenz.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c84610c7a1088e994fc852c64a7893f73f7909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351660"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse

In diesem Abschnitt wird beschrieben, wie Sie Ereignis Referenzseiten (Erps) planen, entwickeln und testen und wie Sie Sie in einem Experten oder Monitor bereitstellen. Weitere Informationen zu Erps und deren Verwendung mit Netzwerkmonitor finden Sie auf der [Seite mit der Ereignis Referenz](event-reference-page.md).

Zum Entwickeln eines neuen ERP besteht der erste Schritt darin, die Ereignisse zu bestimmen, die individuelle Erps für Ihren benutzerdefinierten [Experten](experts.md) oder [Monitor](monitors.md)erfordern. Sie müssen für jedes Ereignis, das Sie in der Netzwerkmonitor Ereignisanzeige anzeigen möchten, separate Erps erstellen. Nehmen Sie beispielsweise Folgendes an:

-   Sie entwickeln einen Monitor mit dem Namen "Game Monitor" und "Stock Watcher".
-   Der Monitor befindet sich in einer Datei namens Gamemon.dll.
-   Der Monitor generiert zwei Ereignisse, die ausgeführt werden, und meine Internet Aktien-Soars.
-   Sie planen, zwei Erps, Gamemon1.htm und Gamemon2.htm zu entwickeln.

> [!Note]  
> Es ist nicht erforderlich, dass Sie über eine 1:1-Entsprechung von Erps verfügen, um Ereignisse zu überwachen oder zu überprüfen.

 

Nachdem Sie eine Liste eindeutiger Erps erstellt haben, führen Sie die folgenden Schritte aus, um die einzelnen ERP-Informationen zu erstellen.

-   [Schreiben Sie das HTML-Quelldokument](writing-an-event-reference-page.md).
-   Speichern Sie die HTML-Quelldatei, [und benennen](naming-an-event-reference-page.md) Sie Sie als eine HTM-Datei.
-   [Testen Sie das ERP](testing-an-event-reference-page.md) mit dem abgeschlossenen Experten oder Monitor.

 

 



