---
title: Neuübertragung wird abgebrochen
description: Wenn innerhalb des Timeout Zeitraums, der für eine Ziel Entität angegeben ist, keine Antwort auf eine Kommunikations Anforderung vorhanden ist, und wenn für die Entität reübertragungen angegeben werden, überträgt die Microsoft WinSNMP-Implementierung die Anforderung erneut.
ms.assetid: 3fd39425-7d57-4bbb-9dcb-f43b6211228c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7346ee6e1e336b4f8fe56df3dce602fe65a0b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036956"
---
# <a name="canceling-retransmission"></a>Neuübertragung wird abgebrochen

Wenn innerhalb des Timeout Zeitraums, der für eine Ziel Entität angegeben ist, keine Antwort auf eine Kommunikations Anforderung vorhanden ist, und wenn für die Entität reübertragungen angegeben werden, überträgt die Microsoft WinSNMP-Implementierung die Anforderung erneut. Ein Aufrufe der [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) -Funktion kann diesen Neuübertragungs-Cycle abbrechen und interne Datenstrukturen freigeben, die der Nachrichten Anforderung zugeordnet sind.

Beachten Sie, dass es möglich ist, dass eine Ziel Entität eine SNMP-Nachricht empfängt, die durch einen Rückruf der [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) -Funktion abgebrochen wurde. Es ist auch möglich, dass eine Ziel Entität auf eine abgebrochene SNMP-Nachricht reagieren kann. Dies liegt daran, dass Transaktions Warteschlangen auf mehreren Ebenen auftreten. Nachdem eine Nachricht jedoch durch einen Aufruf von [**snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)abgebrochen wurde, überträgt die Microsoft WinSNMP-Implementierung die Nachricht nicht erneut, sendet eine Antwort-PDU oder sendet eine Timeout Benachrichtigung an die Anwendung für diese Nachricht.

 

 




