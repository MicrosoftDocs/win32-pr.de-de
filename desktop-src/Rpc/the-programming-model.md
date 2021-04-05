---
title: Das Programmiermodell
description: In den ersten Tagen der Computerprogrammierung wurde jedes Programm als großer monolithischer Block geschrieben, der mit goto-Anweisungen gefüllt wurde.
ms.assetid: b64d5338-a06a-4a27-bedb-c9011fa5a5a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bcc0fd51404290b3d673982001cb3ee91bf1747
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710895"
---
# <a name="the-programming-model"></a>Das Programmiermodell

In den ersten Tagen der Computerprogrammierung wurde jedes Programm als großer monolithischer Block geschrieben, der mit **goto** -Anweisungen gefüllt wurde. Jedes Programm musste seine eigene Eingabe und Ausgabe auf verschiedenen Hardware Geräten verwalten. Als die Programmier Disziplin gereift ist, war dieser monolithische Code in Prozeduren organisiert, wobei die am häufigsten verwendeten Prozeduren in Bibliotheken für Freigabe und Wiederverwendung gepackt wurden.

![monolithische goto-Anweisungen und Prozeduren in freigegebenen Bibliotheken verpackt](images/prog-a06.png)

Die Programmiersprache C unterstützt die Prozedur orientierte Programmierung. In C bezieht sich die Haupt Prozedur auf alle anderen Prozeduren als schwarze Felder. Die Main-Prozedur kann z. B. nicht ermitteln, wie die Prozeduren A, B und X ihre Arbeit erledigen. In der Main-Prozedur wird nur eine andere Prozedur aufgerufen. Sie enthält keine Informationen zur Implementierung dieser Prozedur.

![Isolation von Aktivitäten, die in externen Prozeduren ausgeführt werden](images/prog-a08.png)

Prozedur orientierte Programmiersprachen bieten einfache Mechanismen zum angeben und Schreiben von Prozeduren. Beispielsweise ist der ANSI-Standard-C-Funktionsprototyp ein Konstrukt, mit dem der Name einer Prozedur, der Typ des Ergebnisses, das zurückgegeben wird (sofern vorhanden) und die Anzahl, Sequenz und der Typ der Parameter angegeben werden. Die Verwendung des Funktions Prototyps ist eine formale Methode zum Angeben einer Schnittstelle zwischen Prozeduren.

Microsoft RPC baut auf diesem Programmiermodell auf, indem es in Schnittstellen gruppierte Prozeduren zulässt, die sich in verschiedenen Prozessen befinden als der Aufrufer. Microsoft RPC fügt auch einen formelleren Ansatz für die Prozedur Definition hinzu, der es dem Aufrufer und der aufgerufenen Routine ermöglicht, einen Vertrag zum Remote austauschen von Daten und Aufrufen von Funktionen zu übernehmen Im Microsoft RPC-Programmiermodell werden herkömmliche Funktionsaufrufe mit zwei zusätzlichen Elementen ergänzt.

-   Das erste Element ist eine IDL-/ACF-Datei, die den Datenaustausch und den Parameter Übergabe Mechanismus zwischen dem Aufrufer und der aufgerufenen Prozedur genau beschreibt.
-   Das zweite Element ist ein Satz von Lauf Zeit-APIs, die Entwicklern eine genaue Kontrolle über den Remote Prozedur Aufruf bieten, einschließlich Sicherheitsaspekten, der Verwaltung des Zustands auf dem Server, der Angabe, welche Clients mit dem Server kommunizieren können usw.

 

 




