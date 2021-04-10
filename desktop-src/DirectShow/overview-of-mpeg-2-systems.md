---
description: Übersicht über MPEG-2-Systeme
ms.assetid: 1ebfb194-002f-40ac-9be5-267861b6687b
title: Übersicht über MPEG-2-Systeme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4206b36db7b3172c6e161745922e83490855c73c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125024"
---
# <a name="overview-of-mpeg-2-systems"></a>Übersicht über MPEG-2-Systeme

In diesem Abschnitt erhalten Sie einen allgemeinen, nichttechnischen Überblick über die MPEG-2-Systems-Schicht. MPEG-2-Systeme ist der Standard, der definiert, wie Audiodaten und Videostreams in MPEG-2 multiplext werden.

**Elementare Datenströme**

MPEG-2 Multiplexing beginnt mit einem oder mehreren Bytestreams, die als elementare Streams bezeichnet werden und Video-, Audiodaten oder andere Daten enthalten. Ein Video enthält z. b. komprimierte Videorahmen sowie Sequenz Header, GOP-Header (Group of Image) und andere vom Decoder zum Decodieren des Streams benötigte Elemente. Die Systems-Ebene definiert nicht den Inhalt des es-Byte-Streams.

Ein elementar Datenstrom wird in Pakete aufgeteilt und bildet einen für *packetisiert elementaren Datenstrom* (PES). Die Länge von PES-Paketen ist variabel. Der Inhalt des Pakets wird als *Nutzlast* bezeichnet. Jedes PES-Paket enthält auch einen-Header. Der Multiplexer weist jedem PES eine 1-Byte-Datenstrom-ID zu. einzelne PE-Pakete werden durch die Datenstrom-ID im Paket-Header identifiziert. Für Audiostreams hat die Stream-ID die Form 110 *XXXXX*. Für das Video hat die Stream-ID die Form 1110 *JJJJ*.

Der MPEG-2-Standard definiert zwei Möglichkeiten für die Bereitstellung von in der packetisierten elementaren Datenströme: *Programmstreams* und *Transportstreams*.

**Programmstreams**

Programm Datenströme sind für Umgebungen konzipiert, die relativ fehlerfrei sind, z. b. lokale Dateispeicherung. In einem Programmstream werden die PE-Pakete in Einheiten, die als *Packs* bezeichnet werden, als multiplext und organisiert. Alle PES-Streams in einem Programm Datenstrom werden mit derselben Uhr synchronisiert.

**Transportstreams**

Transport Datenströme (TS) sind für unzuverlässige oder fehleranfällige Umgebungen wie Netzwerkübertragungen konzipiert. Außerdem können Sie mehrere Programme enthalten, die mit unterschiedlichen Uhren synchronisiert werden. Ein Transportstream fügt eine zweite Ebene der packetisierung hinzu – die PES-Streams werden innerhalb von transportstreampaketen verpackt, die eine festgelegte Größe von 188 Bytes pro Paket aufweisen. TS-Pakete können auch Programm Informationsdaten Ströme enthalten, die im folgenden Abschnitt beschrieben werden.

Jedes TS-Paket verfügt über einen 4-Byte-Header und ein optionales Anpassungs Feld, das zusätzliche Header Informationen enthält. Der Multiplexer weist jedem PES-Stream oder Programm Informationsdaten Strom eine Programm-ID (PID) zu. Die PIDs werden verwendet, um die TS-Pakete zu identifizieren, ähnlich der Art und Weise, wie Stream-IDs PE-Pakete identifizieren. (Wenn ein Transportstream mehrere Programme enthält, sind die *Stream* -IDs möglicherweise nicht eindeutig, aber die PID-Zuweisungen sind innerhalb des Transportstreams eindeutig.)

**Programm spezifische Informationen**

Da ein Transportstream mehrere Programme enthalten kann, muss es eine Möglichkeit geben, die verschiedenen PES-Pakete den Programmen zuzuordnen, denen Sie angehören. Dies erfolgt mithilfe von Tabellen, mit denen die Programmstreams identifiziert werden. Gemeinsam werden diese Daten als Programm spezifische Informationen (PSI) bezeichnet. Die PSI-Daten werden wie die Daten der Daten in TS-Paketen übertragen. Es gibt verschiedene Arten von PSI-Daten, einschließlich:

-   Programm Zuordnungs Tabelle (Pat). Pat wird immer PID 0x000 zugewiesen. Jeder Eintrag in Pat ist eine PID, die die PMT-Pakete für dieses Programm identifiziert (siehe nächstes Element).
-   Programm Zuordnungs Tabelle (PMT). Jedes PMT definiert ein Programm. Das PMT enthält eine Liste von Streams. jeder Tabelleneintrag gibt die PID für diesen Stream sowie einen Code an, der den Streamtyp identifiziert. ISO/IEC 13818-1 definiert einige standardstreamtypen. in der folgenden Tabelle wird eine abgekürzte Liste angezeigt.

    | \_Streamtyp | BESCHREIBUNG  |
    |--------------|--------------|
    | 0x01         | MPEG-1-Video |
    | 0x02         | MPEG-2-Video |
    | 0x03         | MPEG-1-Audiodatei |
    | 0x04         | MPEG-2-Audiodatei |
    | 0x80-0xFF  | Benutzer privat |

    

     

    Andere Standards, die auf MPEG-2 basieren, z. b. ATSC, können zusätzliche Streamtypen im Bereich "Benutzer privat" definieren. ATSC definiert z. b. 0x81 als Dolby AC-3-Audiodatei.

-   Bedingte Zugriffs Tabellen (CAT)
-   Netzwerk Identifizierungs Tabellen (NIT)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MPEG-2-Unterstützung in DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



