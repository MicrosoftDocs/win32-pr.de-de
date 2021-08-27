---
description: Vorteile von DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Vorteile von DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b13a9ef7f91446d03732b935648b689ab65a33c9d10dcfca26051d9284404db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103370"
---
# <a name="benefits-of-dmos"></a>Vorteile von DMOs

DMOs bieten die folgenden Vorteile:

-   Sie sind im Allgemeinen kleiner und einfacher als DirectShow-Filter, da sie weniger Funktionalität unterstützen.
-   Sie sind flexibler als DirectShow-Filter, da sie kein Filterdiagramm erfordern. Sie können sie mit DirectShow verwenden, wenn Sie die von DirectShow zur Verfügung gestellten Dienste benötigen, z. B. Synchronisierung, intelligente Verbindung, automatische Verarbeitung des Datenflusses und Threadverwaltung. Clients, die diese Dienste nicht benötigen, können direkt auf DMOs zugreifen.
-   DMOs führen immer eine synchrone Datenverarbeitung durch, wodurch viele Threadingprobleme vermieden werden, die Sie beim Schreiben eines Filters berücksichtigen müssen.
-   Im Gegensatz zu herkömmlichen ACM- und VCM-Codecs basieren DMOs auf dem Component Object Model (COM), sodass sie über **QueryInterface** erweitert werden können.
-   DMOs unterstützen ein allgemeineres Streamingmodell als ACM- oder VCM-Codecs. Wie DirectShow-Filter können DMOs mehrere Eingaben und ausgaben unterstützen.

Aus diesen Gründen werden DMOs jetzt als Lösung zum Schreiben von Encodern, Decodern und Audioeffekten empfohlen. Abhängig von den Anforderungen der Anwendung sind auch viele andere Szenarien möglich.

Unterschiede zwischen DMOs und DirectShow-Filtern

DirectShow-Filter können nicht außerhalb eines DirectShow-Filterdiagramms funktionieren. In DirectShow vermittelt der Filter Graph Manager zwischen der Anwendung und den Filtern. DirectShow-Filter erledigen den Großteil der zum Streamen von Daten erforderlichen Arbeit, einschließlich:

-   Zuordnen von Puffern.
-   Aushandeln von Medientypen und Verbindungen mit anderen Filtern.
-   Pushen von Daten durch das Filterdiagramm.
-   Senden von Ereignissen an den Filter Graph Manager.
-   Synchronisieren mehrerer Threads.

Im Gegensatz dazu führt ein DMO keine dieser Vorgänge aus. Stattdessen liegen diese Aufgaben in der Verantwortung des Clients, der die DMO verwendet. Der Client ordnet Puffer zu, füllt sie mit Daten auf und übermittelt sie an die DMO. Der DMO verarbeitet die Daten, und der Client ruft die resultierenden Ausgabepuffer ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu DMOs](about-dmos.md)
</dt> </dl>

 

 



