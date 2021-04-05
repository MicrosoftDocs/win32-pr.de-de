---
title: Abrufen einer Codierungs Identität
description: Eine Anwendung, die codierte Daten decodiert, kann die Identität der Routine abrufen, die zum Codieren der Daten verwendet wird, bevor eine Routine zum Decodieren aufgerufen wird. Diese Identität wird von der mesinqprocencodingid-Routine bereitstellt.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Abrufen der Codierungs Identität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713073"
---
# <a name="obtaining-an-encoding-identity"></a>Abrufen einer Codierungs Identität

Eine Anwendung, die codierte Daten decodiert, kann die Identität der Routine abrufen, die zum Codieren der Daten verwendet wird, bevor eine Routine zum Decodieren aufgerufen wird. Diese Identität wird von der [**mesinqprocencodingid**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) -Routine bereitstellt.

Jeder Prozedur in einer Schnittstelle wird vom Mittelwert Compiler eine ganzzahlige Identifikationsnummer, die als *Prozedur Bezeichner* oder eine *proc ID* bezeichnet wird, zugewiesen. Die Nummerierung beginnt mit 0. Die RPC-Laufzeitbibliotheken sind nicht an der Übersetzung der Prozedur-ID in einen tatsächlichen Prozedur Aufruf beteiligt. Wenn eine proc ID angegeben ist, muss Ihre Anwendung eine Möglichkeit zum Aufrufen der richtigen Prozedur bereitstellen. In der Regel verwenden Anwendungsentwickler eine Reihe von **if** -Anweisungen oder (bei Verwendung von C/C++) eine **Switch** -Anweisung zu diesem Zweck.

 

 




