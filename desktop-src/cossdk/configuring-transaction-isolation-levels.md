---
description: Com+ ermöglicht Entwicklern eine bessere Kontrolle über Ihre Anwendungen, indem konfigurierbare Transaktions Isolations Stufen zugelassen werden.
ms.assetid: a59e262c-41f2-4c80-a04c-50a39af8b009
title: Konfigurieren von Transaktions Isolations Stufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d789b9eaed6dfdd2f2419c7eae391d628e75b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483054"
---
# <a name="configuring-transaction-isolation-levels"></a>Konfigurieren von Transaktions Isolations Stufen

Com+ ermöglicht Entwicklern eine bessere Kontrolle über Ihre Anwendungen, indem konfigurierbare Transaktions Isolations Stufen zugelassen werden. Versionen von com+ vor com+ 1,5 verwendeten stets die höchste Isolationsstufe für Transaktionen. Diese Ebene gewährleistet, dass die Datenintegrität immer beibehalten wird. Dies kann jedoch zu Leistungsproblemen führen, wie z. b. Timeouts, wenn viele Transaktionen für eine große Datenbank ausgeführt werden müssen. Mit konfigurierbaren Isolations Stufen können erfahrene Entwickler die Parallelität erhöhen, um die Leistung und Skalierbarkeit zu verbessern.

Com+ bietet die folgenden Transaktions Isolations Stufen.



| Ebene            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Serialisierte       | Von einer aktuellen Transaktion gelesene Daten können erst durch eine andere Transaktion geändert werden, wenn die aktuelle Transaktion abgeschlossen ist. Es können keine neuen Daten eingefügt werden, die sich auf die aktuelle Transaktion auswirken würden. Dies ist die sicherste Isolationsstufe und ist die Standardeinstellung.                                                                                                                                                                                                                                                                                                                                                    |
| Repeatable Read  | Von einer aktuellen Transaktion gelesene Daten können erst durch eine andere Transaktion geändert werden, wenn die aktuelle Transaktion abgeschlossen ist. Jeder Typ neuer Daten kann während einer Transaktion eingefügt werden.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Read Committed   | Eine Transaktion kann keine Daten lesen, die von einer anderen Transaktion geändert werden, für die kein Commit ausgeführt wurde. Dies ist die Standard Isolationsstufe in Microsoft SQL Server.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Read Uncommitted | Eine Transaktion kann beliebige Daten lesen, auch wenn Sie durch eine andere Transaktion geändert wird. Dies ist die am wenigsten sichere Isolationsstufe, lässt jedoch die höchste Parallelität zu.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Any              | Jede Isolationsstufe wird unterstützt. Diese Einstellung wird am häufigsten von Downstreamkomponenten verwendet, um Konflikte zu vermeiden. Diese Einstellung ist nützlich, da jede Downstreamkomponente mit einer Isolationsstufe konfiguriert werden muss, die kleiner oder gleich der Isolationsstufe der unmittelbaren Upstreamkomponente ist. Daher verwendet eine Downstreamkomponente, deren Isolationsstufe als any konfiguriert ist, immer dieselbe Isolationsstufe, die von der unmittelbaren Upstreamkomponente verwendet wird. Wenn für das Stamm Objekt in einer Transaktion die Isolationsstufe konfiguriert ist, wird die Isolationsstufe serialisiert. |



 

> [!Note]  
> Wenn eine Downstreamkomponente mit einer höheren Isolationsstufe als eine Upstreamkomponente konfiguriert ist und versucht, eine Transaktion in eine Transaktion einzutragen, werden Fehler Ergebnisse und die Transaktion abgebrochen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Transaktionsisolationsstufe](setting-the-transaction-isolation-level.md)
</dt> </dl>

 

 



