---
title: Netzwerk Ablauf Verfolgung in Windows 7-Architektur
description: Die folgende Abbildung zeigt die grundlegende Architektur der Netzwerk Ablauf Verfolgung in Windows 7.
ms.assetid: b3023469-0f98-451c-b39f-c3eae771eacc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41221ebf434c05a8c9b7c8489e861128029b5320
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339296"
---
# <a name="network-tracing-in-windows-7-architecture"></a>Netzwerk Ablauf Verfolgung in Windows 7: Architektur

Die folgende Abbildung zeigt die grundlegende Architektur der Netzwerk Ablauf Verfolgung in Windows 7.

![Architektur Diagramm der Netzwerk Ablauf Verfolgung](images/ut1.png)

Die Netzwerk Ablauf Verfolgung nutzt das in Windows verfügbare etw-Framework (Event Tracing for Windows). Netzwerkkomponenten (z. b. Winsock, TCP/IP, NDIS, Paket Erfassung usw.) registrieren sich als etw-Ablauf Verfolgungs Anbieter und geben Ereignisse im Zusammenhang mit der Netzwerkaktivität aus. Jede beschreibbare Aktivität von Bedeutung kann ein Ereignis sein, das an etw protokolliert wird. Die Ablauf Verfolgung für diese Netzwerkkomponenten und Paket Erfassungen kann mit dem **netsh** -Ablauf Verfolgungs Kontext aktiviert werden, der als etw-Controller fungiert.

Die generierten Ablauf Verfolgungen werden in einer ETL-Datei (Event Trace Log, Ereignis Ablauf Verfolgungs Protokoll) gesammelt. Diese ETL-Dateien können dann mit einer Reihe von Tools analysiert werden, z. b. Netzwerkmonitor 3,2 und höher, Ereignisanzeige, **Netsh Trace Convert** oder Tracerpt.exe.

Jedes ETW-Ereignis verfügt über einen allgemeinen Header, bei dem etw Informationen speichert, z. b. die Ereignis Eigenschaften, Zeitstempel und die Aktivitäts-ID. (Weitere Informationen zu Aktivitäts-IDs finden [Sie unterschreiben verwandter Ereignisse in einem End-to-End-Szenario](../etw/writing-related-events-in-an-end-to-end-scenario.md)). Die Aktivitäts-ID wird verwendet, um Ereignisse zu korrelieren. Im Benutzermodus werden Aktivitäts-IDs in Threads gespeichert, und alle Ereignisse, die in einem Thread protokolliert werden, werden automatisch mit der gleichen Aktivitäts-ID gekennzeichnet. Im Kernel Modus muss die Aktivitäts-ID explizit übermittelt werden, wenn ein Ereignis protokolliert wird. ETL-Dateien werden standardmäßig zusammen mit den Gruppen Ereignissen unter bestimmten Aktivitäts-IDs korreliert.

Weitere Informationen zu Windows-Ereignissen und etw finden Sie unter [Windows-Ereignisse](../events/windows-events.md).

## <a name="etw-components-in-network-tracing"></a>Etw-Komponenten in der Netzwerk Ablauf Verfolgung

Die Netzwerk Ablauf Verfolgung verwendet etw als primären Ablauf Verfolgungs Mechanismus, um Informationen über die Vorgänge der Netzwerk Subsysteme bereitzustellen. Etw umfasst vier Hauptkomponenten: Ereignis Ablauf Verfolgungs Sitzungen, Ereignis Anbieter, Ereignis Controller und Ereignisconsumer.

Pufferung und Protokollierung erfolgen in *Ereignis Ablauf Verfolgungs Sitzungen*, bei denen Ereignisse von Anbietern akzeptiert und Ablauf Verfolgungs Dateien erstellt werden.

Ein *Ereignis Anbieter* ist eine logische Entität, die Ereignisse in ETW-Sitzungen schreibt. Ein Ereignis Anbieter kann eine Benutzermodusanwendung, eine verwaltete Anwendung, ein Treiber oder eine beliebige andere Software Entität sein. Ereignis Anbieter registrieren sich bei etw und schreiben Ereignisse aus verschiedenen Punkten im Code, indem Sie die ETW-Protokollierungs-API aufrufen. Aufgrund der wachsenden Ereignis Instrumentation in vielen Betriebssystemkomponenten enthält auch eine einfache Anwendung oder ein Szenario in Windows mehrere Komponenten, bei denen es sich um Ereignis Anbieter handelt.

Ein *Ereignis Controller* startet und beendet Ereignis Ablauf Verfolgungs Sitzungen und ermöglicht Anbieter. Wenn ein Ereignis Anbieter dynamisch von der Ereignis Controller Anwendung aktiviert wird, sendet der Anbieter Ereignisse an eine bestimmte Ereignis Ablauf Verfolgungs Sitzung, die vom Ereignis Controller festgelegt wird. Jedes Ereignis, das vom Ereignis Anbieter an die Ereignis Ablauf Verfolgungs Sitzung gesendet wird, besteht aus einem Fixed-Header, der Ereignis Metadaten und alle zusätzlichen benutzerdefinierten Daten enthält, die vom Anbieter protokolliert werden.

Ein *Ereignisconsumer* ist eine Anwendung, die Protokolldateien liest oder eine Ereignis Ablauf Verfolgungs Sitzung für Echtzeitereignisse abhört und verarbeitet. Ein Beispiel für einen Ereignisconsumer ist Microsoft-Netzwerkmonitor 3,2, der die Fähigkeit zum Lesen und Anzeigen von Protokolldateien enthält, die von der Netzwerk Ablauf Verfolgung in Windows 7 erstellt werden.

Ereignisse werden in chronologischer Reihenfolge an Ereignisconsumer übermittelt, und es gibt verschiedene ereignisconsumeranwendungen, in denen die Ereignisse in bestimmten Formaten angezeigt werden. Wenn ein Ereignis in einer Sitzung protokolliert wird, fügt ETW dem Ereignis Header zusätzliche Informationen hinzu, einschließlich Zeitstempel, Prozess-und Thread-ID, Prozessornummer und CPU-Nutzungsdaten des Protokollierungs Threads. Diese Daten werden dann zusammen mit allen benutzerdefinierten Daten, die vom Anbieter eingeschlossen werden, an Ereignisconsumer weitergeleitet.

Anbieter, die die neuen [Ereignis Protokollierungs-APIs](/windows/win32/api/evntprov/nf-evntprov-eventwrite) verwenden, müssen eine XML-Datei bereitstellen, die als [Ereignis Manifest](../wes/eventschema-schema.md)bezeichnet wird. Diese Datei enthält Metadaten, mit denen alle benutzerdefinierten Daten und Layoutinformationen für die vom Anbieter geschriebenen Ereignisse definiert werden. Eine allgemeine Consumeranwendung verwendet dann die APIs für das [Trace Data Helper (TDH)](/windows/win32/api/tdh/) , um die Ereignis Metadaten abzurufen, die Ereignisse zu decodieren und anzuzeigen.

Mit der Netzwerk Ablauf Verfolgung in Windows 7 umfasst die Ereignis Controller-/consumerseite eine End-to-End-szenariobasierte Ablauf Verfolgungs Unterstützung, die in die Windows-Diagnose-und-Support Umgebungen integriert ist Ein Szenario definiert eine Sammlung von Ereignis Anbietern, die an dem Szenario beteiligt sind. Die Ereignis Controller/consumerseite definiert die Szenarien (Kontexte), in denen die Ablauf Verfolgung verwendet werden kann, einschließlich der relevanten Anbieter für bestimmte Szenarien über Netzwerkkomponenten hinweg. Die Ereignis Anbieterseite enthält standardisierte Netzwerkablaufverfolgungs-Ereignisse aus verschiedenen Komponenten im Netzwerk Stapel, die über etw-Aktivitäts-IDs korreliert werden können. Die Anbieter verwenden ein gängiges Netzwerk Schema, das die Verwendung von etw-Konzepten, wie z. b. Schlüsselwörtern, Ebenen, Tasks und Opcodes, standardisiert. Das Schema definiert auch Ereignisse, die für viele Netzwerkkomponenten (z. b. Fehlerereignisse, Paket Lösch Ereignisse, Schema Ereignisse und Zustands Übergangs Ereignisse) üblich sind.

 

 