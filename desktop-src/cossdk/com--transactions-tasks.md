---
description: Aufgaben für COM+-Transaktionen
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Aufgaben für COM+-Transaktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127153"
---
# <a name="com-transactions-tasks"></a>Aufgaben für COM+-Transaktionen

Die automatische Transaktionsverarbeitung in com+ ermöglicht es Ihnen, eine produktivere Entwicklungszeit beim Erstellen und Konfigurieren von Objekten auszugeben, die an automatischen Transaktionen teilnehmen sollen. es gibt jedoch einige Programmieraufgaben, die Sie ausführen können, um das Transaktionsverhalten an Ihre Anwendungsanforderungen anzupassen.

In den folgenden Themen werden bestimmte Programmier Optionen im Zusammenhang mit der Transaktionsverarbeitung erörtert.



| Thema                                                                                             | BESCHREIBUNG                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Festlegen des Transaktions Attributs](setting-the-transaction-attribute.md)<br/>             | Beschreibt, wie Transaktions Attributwerte für die Transaktions Objekte festgelegt werden.<br/>         |
| [Festlegen der Transaktionsisolationsstufe](setting-the-transaction-isolation-level.md)<br/> | Beschreibt, wie die Transaktions Isolations Stufen für die Transaktions Objekte festgelegt werden.<br/>     |
| [Festlegen des Transaktions Timeouts](setting-the-transaction-time-out.md)<br/>               | Beschreibt, wie Timeout Intervalle für Ihre Transaktionen festgelegt werden.<br/>                          |
| [Festlegen der konsistenten und done-Flags](setting-the-consistent-and-done-flags.md)<br/>     | Zeigt, wie die konsistenten und done-Flags verwendet werden, um das Ergebnis einer Transaktion zu steuern.<br/> |
| [Erstellen von BYOT-Objekten](creating-byot-objects.md)<br/>                                     | Beschreibt, wie Objekte erstellt werden, sodass Sie Ihre eigene Transaktion (BYOT) einbringen können.<br/>           |



 

> [!Note]  
> Als allgemeine Regel gilt, dass alle Komponenten, die einen persistenten Zustand aktualisieren, Transaktionen unterstützen sollten. Komponenten, die die Vorgänge von zwei oder mehr Objekten in einer einzigen Aufgabe kombinieren, sollten Transaktionen verwenden, um die Fehlerwiederherstellung zu vereinfachen. Zum Freigeben von Ressourcen, wie z. b. Datenbankverbindungen, sollten Transaktionen in com+ so kurz sein, wie Sie Sie vornehmen können.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der com+-Transaktionen](com--transactions-concepts.md)
</dt> </dl>

 

 




