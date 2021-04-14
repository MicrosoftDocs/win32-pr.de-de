---
description: Sie können die Auswirkung ihrer Anwendung auf andere Clients und deren Auswirkungen auf Ihre Anwendung minimieren, indem Sie so viele Freigabe Möglichkeiten wie möglich gewähren, die erforderliche Mindestzugriffsebene anfordern und die am wenigsten eindringliche opportunistische Sperre verwenden, die für Ihre Anwendung geeignet ist.
ms.assetid: c28b0ae0-0d35-4b59-9f54-87c55ca72716
title: Server Antwort auf geöffnete Anforderungen für gesperrte Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d397613f6b54f2b42c26a5674a787b796f5f19e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526858"
---
# <a name="server-response-to-open-requests-on-locked-files"></a>Server Antwort auf geöffnete Anforderungen für gesperrte Dateien

Die Lebensdauer einer opportunistischen Sperre umfasst drei verschiedene Zeitspannen. Während jedes wird der Server unterschiedlich festgelegt, um seine Reaktion auf eine Anforderung von einem Client zum Öffnen einer Datei zu öffnen, die von einem anderen Client gesperrt wurde. Im Allgemeinen können Sie die Auswirkung ihrer Anwendung auf andere Clients und deren Auswirkungen auf Ihre Anwendung minimieren, indem Sie so viele gemeinsame Freigaben wie möglich gewähren, die erforderliche Mindestzugriffsebene anfordern und die am wenigsten geeignete opportunistische Sperre verwenden, die für Ihre Anwendung geeignet ist.

Der erste Punkt ist der Zeitraum, nach dem der Server eine Datei für einen Client öffnet, aber bevor er eine Sperre erteilt. Während dieser Zeit ist keine Sperre für die Datei vorhanden, und der Server hängt von Freigabe, Zugriffs Modi und Art der opportunistischen Sperre ab, die Sie anfordern, um die Reaktion auf eine andere Anforderung zum Öffnen der gleichen Datei zu bestimmen. Wenn Sie z. b. die betreffende Datei für den Schreibzugriff öffnen, können Sie die Gewährung von opportunistischen Sperren unterbinden, die Lese Cache Zugriff auf andere Clients ermöglichen. Die Zeitspanne, bevor der Server eine Sperre gewährt, befindet sich in der Regel im Millisekundenbereich, kann aber länger sein.

Nachdem die opportunistische Sperre erteilt wurde, überprüft der Server die Sperre, um die Server Reaktion auf eine geöffnete Anforderung für eine gesperrte Datei zu bestimmen. Auch hier gilt: wie die Anwendung die Datei geöffnet hat und welche Art von Sperre Sie enthält, wirkt sich darauf aus, wie der Server antwortet. Weitere Informationen dazu, wie der Server in jedem Fall antwortet, finden Sie unter [Typen von opportunistischen Sperren](types-of-opportunistic-locks.md).

Schließlich gibt es die Spanne, nachdem der Server festgelegt hat, dass die Sperre beschädigt (beendet) werden soll, aber bevor die Anwendung die Reaktion auf die Unterbrechung abschließt. Abhängig von der Art der Sperre kann die Anwendung die Sperre auf eine niedrigere Ebene oder überhaupt auf None herabstufen. Die Anwendung kann auch die Datei und die Sperre schließen. Während dieser Zeit hält der Server sämtliche Anforderungen von anderen Clients an, um die zuvor gesperrte Datei zu öffnen. Diese Zeitspanne kann zwischen Millisekunden und zehn Sekunden liegen. Weitere Informationen finden Sie unter unter [brechen von opportunistischen Sperren](breaking-opportunistic-locks.md).

 

 



