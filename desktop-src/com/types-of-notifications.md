---
title: Benachrichtigungs Typen
description: Benachrichtigungs Typen
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388582"
---
# <a name="types-of-notifications"></a>Benachrichtigungs Typen

Benachrichtigungen werden in drei Gruppen unterteilt: Verbund Dokument, Daten und Ansicht. Ein-Objekt sendet Verbund Dokument Benachrichtigungen als Antwort auf die Umbenennung, Speicherung, Schließung oder im Fall eines Links, wenn die zugehörige Verknüpfungs Quelle umbenannt wurde. Wie Sie erwarten, senden-Objekte Daten Benachrichtigungen als Reaktion auf Änderungen in Ihren Daten und senden Anzeige Benachrichtigungen als Reaktion auf Änderungen in der Präsentation. Container Anwendungen müssen für jeden dieser Benachrichtigungs Typen separat registriert werden, aber alle können von einer einzelnen Beratungs Senke verarbeitet werden.

Alle Container, der Objekt Handler und das verknüpfte Objekt werden für Verbund Dokument Benachrichtigungen registriert. Der typische Container wird auch für Anzeige Benachrichtigungen registriert. Daten Benachrichtigungen werden normalerweise an das verknüpfte Objekt und den Objekt Handler gesendet. Ein spezieller Container, z. b. ein Container, der die Daten selbst rendert, kann vom Empfang von Daten Benachrichtigungen anstelle von Anzeige Benachrichtigungen profitieren. Beispielsweise kann ein eingebetteter Diagramm Container mit einem Link zu einer Tabelle für Daten Benachrichtigungen registriert werden. Da sich eine Änderung an der Tabelle auf das Diagramm auswirkt, würde der Empfang einer Daten Benachrichtigung den Container dazu leiten, die neuen tabellarischen Daten zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Benachrichtigungen](notifications.md)
</dt> </dl>

 

 




