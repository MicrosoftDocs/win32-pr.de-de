---
title: Einführung in die RPC-Speicherverwaltung
description: Einführung in die Speicherverwaltung für Remote Prozedur Aufrufe (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316064"
---
# <a name="introduction-to-rpc-memory-management"></a>Einführung in die RPC-Speicherverwaltung

Im Zusammenhang mit RPC umfasst die Speicherverwaltung Folgendes:

-   Zuweisen und Aufheben der Zuordnung des Speichers, der zum Simulieren eines einzelnen konzeptionellen Adressraums zwischen dem Client und dem Server in den unterschiedlichen Adressräumen der Client-und Serverthreads benötigt wird.
-   Ermitteln der Softwarekomponente, die für die Verwaltung des Arbeitsspeichers zuständig ist – der Anwendung oder dem von der Mitte generierten Stub.
-   Auswählen von "Mittel l"-Attributen, die sich auf die Speicherverwaltung auswirken: Direktionale Attribute, Zeiger Attribute, Array Attribute und die ACF-Attribute \[ [Byte \_ Anzahl](/windows/desktop/Midl/byte-count) \] , \[ [zuordnen](/windows/desktop/Midl/allocate) \] und \[ [Aktivierung \_ ](/windows/desktop/Midl/enable-allocate) \] von Zuordnungen.

Wenn ein Programm eine Funktion oder Prozedur im Adressraum aufruft, ist die Speicherverwaltung einfacher als in einer verteilten Anwendung. Um dies zu veranschaulichen, stellt das folgende Diagramm eine binäre Struktur dar. Um diese Datenstruktur an eine Prozedur im Adressraum zu übergeben, übergibt ein Programm einfach einen Zeiger an den Stamm der Struktur.

![eine binäre Struktur mit Zeigern auf Strukturdaten, die im Stamm der Struktur abgelegt sind.](images/bintree.png)

Client-/Server-RPC-Anwendungen nutzen Daten über zwei verschiedene Speicherplätze hinweg gemeinsam. Diese Speicherplätze können sich auf demselben Computer befinden oder nicht. Der Client und der Server haben in beiden Fällen keinen direkten Zugriff auf den Arbeitsspeicher Bereich der anderen. RPC hängt von der Fähigkeit ab, den Adressraum des Client Programms im Adressraum des Server Programms zu simulieren. Außerdem müssen Daten, einschließlich neuer und geänderter Daten, vom Server in den Client Speicher zurückgegeben werden.

In Fällen wie der binär Struktur, die im vorangehenden Diagramm dargestellt ist, reicht es nicht aus, einen Zeiger auf den Stamm Knoten an eine Remote Prozedur zu übergeben. Entweder das Programm oder die Stub muss die gesamte Struktur an den Adressbereich des Servers übergeben, damit das Remote Verfahren darauf angewendet werden kann.

 

 