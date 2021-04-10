---
description: Vorteile von dmos
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Vorteile von dmos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213964"
---
# <a name="benefits-of-dmos"></a>Vorteile von dmos

DMOS bietet die folgenden Vorteile:

-   Sie sind im Allgemeinen kleiner und einfacher als DirectShow-Filter, da Sie weniger Funktionen unterstützen.
-   Sie sind flexibler als DirectShow-Filter, da Sie kein Filter Diagramm benötigen. Sie können Sie mit DirectShow verwenden, wenn Sie die von DirectShow bereitgestellten Dienste benötigen, z. b. Synchronisierung, intelligente Verbindung, automatische Verarbeitung des Datenflusses und Thread Verwaltung. Clients, die diese Dienste nicht benötigen, können direkt auf DMOS zugreifen.
-   DMOS führt immer eine synchrone Datenverarbeitung durch, wodurch viele der Threading Probleme vermieden werden, die Sie beim Schreiben eines Filters beachten müssen.
-   Im Gegensatz zu herkömmlichen ACM-und VCM-Codecs basieren DMOS auf dem Component Object Model (com), sodass Sie über **QueryInterface** erweitert werden können.
-   DMOS unterstützen ein generalisiertes Streamingmodell als ACM-oder VCM-Codecs. Wie DirectShow-Filter kann DMOS mehrere Eingaben und mehrere Ausgaben unterstützen.

Aus diesen Gründen werden DMOS nun als Lösung für das Schreiben von Encodern, Decodern und Audioeffekten empfohlen. Viele andere Szenarien sind auch möglich, abhängig von den Anforderungen der Anwendung.

Unterschiede zwischen DMOS und DirectShow-Filtern

DirectShow-Filter können nicht außerhalb eines DirectShow-Filter Diagramms funktionieren. In DirectShow wird der Filter Graph-Manager zwischen der Anwendung und den Filtern mediiert. DirectShow-Filter führen den größten Teil der Arbeit aus, die zum Streamen von Daten erforderlich ist, einschließlich:

-   Puffer werden zugeordnet.
-   Aushandeln von Medientypen und Verbindungen mit anderen Filtern.
-   Übertragen von Daten über das Filter Diagramm
-   Senden von Ereignissen an den Filter Diagramm-Manager.
-   Synchronisieren mehrerer Threads.

Im Gegensatz dazu führt ein DMO keines dieser Dinge aus. Stattdessen sind diese Arten von Aufgaben für den Client mit dem DMO verantwortlich. Der Client ordnet Puffer zu, füllt sie mit Daten und übergibt sie an den DMO. Der DMO verarbeitet die Daten, und der Client ruft die resultierenden Ausgabepuffer ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DMOS](about-dmos.md)
</dt> </dl>

 

 



