---
title: Abrufen einer Codierungsidentität
description: Eine Anwendung, die codierte Daten decodiert, kann die Identität der Routine abrufen, die zum Codieren der Daten verwendet wird, bevor eine Routine zum Decodieren der Daten aufruft. Die MesInqProcEncodingId-Routine stellt diese Identität zur Auswahl.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- REMOTE PROCEDURE Call RPC , Tasks, Abrufen der Codierungsidentität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a0883a1a032a76f13cfeeb6c5d6a8923146b7ee9e8184d37d5994fb5e328bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019447"
---
# <a name="obtaining-an-encoding-identity"></a>Abrufen einer Codierungsidentität

Eine Anwendung, die codierte Daten decodiert, kann die Identität der Routine abrufen, die zum Codieren der Daten verwendet wird, bevor eine Routine zum Decodieren der Daten aufruft. Die [**MesInqProcEncodingId-Routine**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) stellt diese Identität zur Auswahl.

Jeder Prozedur in einer Schnittstelle wird vom MIDL-Compiler eine ganzzahlige ID zugewiesen, die als Prozedurbezeichner oder Prozedur-ID bezeichnet wird.   Die Nummerierung beginnt mit 0 (null). Die RPC-Laufzeitbibliotheken sind nicht an der Übersetzung der Prozedur-ID in einen tatsächlichen Prozeduraufruf beteiligt. Bei einer Prozedur-ID muss Ihre Anwendung eine Möglichkeit zum Aufrufen der richtigen Prozedur bereitstellen. Anwendungsentwickler verwenden in der Regel  eine Reihe von if-Anweisungen oder (bei Verwendung von C/C++) eine **switch-Anweisung** für diesen Zweck.

 

 




