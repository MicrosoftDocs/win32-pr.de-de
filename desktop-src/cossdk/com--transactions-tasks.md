---
description: COM+-Transaktionsaufgaben
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: COM+-Transaktionsaufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102b0ec6ae54430be5499c67b5041ee26035eb077e27b1b860377cd728e3e42d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307590"
---
# <a name="com-transactions-tasks"></a>COM+-Transaktionsaufgaben

Während die automatische Transaktionsverarbeitung in COM+ ihnen ermöglicht, produktivere Entwicklungszeit für das Erstellen und Konfigurieren von Objekten zu verbringen, die Sie an automatischen Transaktionen teilnehmen möchten, gibt es einige Programmieraufgaben, die Sie ausführen können, um das Transaktionsverhalten an Ihre Anwendungsanforderungen anzupassen.

In den folgenden Themen werden bestimmte Programmieroptionen im Zusammenhang mit der Transaktionsverarbeitung behandelt.



| Thema                                                                                             | BESCHREIBUNG                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Festlegen des Transaktionsattributs](setting-the-transaction-attribute.md)<br/>             | Beschreibt, wie Transaktionsattributwerte für Ihre Transaktionsobjekte festgelegt werden.<br/>         |
| [Festlegen der Transaktionsisolationsstufe](setting-the-transaction-isolation-level.md)<br/> | Beschreibt, wie die Transaktionsisolationsstufen für Ihre Transaktionsobjekte festgelegt werden.<br/>     |
| [Festlegen des Transaktions-Time out](setting-the-transaction-time-out.md)<br/>               | Beschreibt, wie Time out-Intervalle für Ihre Transaktionen festgelegt werden.<br/>                          |
| [Festlegen der Flags "Konsistent" und "Fertig"](setting-the-consistent-and-done-flags.md)<br/>     | Zeigt, wie sie die flags consistent und done verwenden, um das Ergebnis einer Transaktion zu steuern.<br/> |
| [Erstellen von BYOT-Objekten](creating-byot-objects.md)<br/>                                     | Beschreibt, wie Objekte erstellt werden, damit Sie Bring Your Own Transaction (BYOT) verwenden können.<br/>           |



 

> [!Note]  
> Im Allgemeinen sollte jede Komponente, die den persistenten Zustand aktualisiert, Transaktionen unterstützen. Komponenten, die die Vorgänge von zwei oder mehr Objekten zu einem einzelnen Task kombinieren, sollten Transaktionen verwenden, um die Fehlerwiederherstellung zu vereinfachen. Außerdem sollten Transaktionen in COM+ so kurz wie möglich sein, um Ressourcen wie Datenbankverbindungen frei zu machen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Transaktionskonzepte](com--transactions-concepts.md)
</dt> </dl>

 

 




