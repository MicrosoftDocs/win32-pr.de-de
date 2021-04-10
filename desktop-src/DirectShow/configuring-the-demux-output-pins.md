---
description: Konfigurieren der Demux-Ausgabe Pins
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Konfigurieren der Demux-Ausgabe Pins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56a24af3f49f26efe4ff6afad075a3cef61fcd1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124873"
---
# <a name="configuring-the-demux-output-pins"></a>Konfigurieren der Demux-Ausgabe Pins

Wenn MPEG-2 Demux ein Datenpaket empfängt, muss es bestimmen, welche Ausgabepin analysiert und die Daten übermitteln soll. Im Programm Datenstrom Modus ordnet das Demux Stream-IDs den Ausgabe Pins zu. Im transportstreammodus werden PIDs den Ausgabe Pins zugeordnet. Wenn z. b. im transportstreammodus die PID 0x31 Pin 0 zugeordnet ist, wird jedes TS-Paket mit dieser PID-Nummer an die Ausgabe-PIN 0 weitergeleitet. Wenn die Demux ein Paket empfängt, dessen Stream-ID oder PID keiner Ausgabe-PIN zugeordnet ist, wird das Paket einfach verworfen.

Im Pullmodus erstellt das Demux automatisch Ausgabe Pins für die Audiodaten und Videostreams in der Datei und ordnet die Stream-IDs den Pins zu.

Im Pushmodus müssen die Ausgabe Pins von der Anwendung oder einem anderen Filter konfiguriert werden. Bei digitalen Fernseh Quellen, die die Broadcast Driver Architecture (BCM) verwenden, funktioniert der Filter des Netzwerk Anbieters mit dem TIF-Filter, um die-Funktion zu konfigurieren. Die Anwendung muss nichts Unternehmen. In anderen Szenarien muss die Anwendung die Ausgabe Pins konfigurieren.

Die Demux beginnt ohne Ausgabe Pins. Um eine Ausgabe-PIN zu erstellen, rufen Sie die [**IMpeg2Demultiplexer:: up-outputpin**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) -Methode für den Filter auf. Diese Methode nimmt einen Medientyp und einen Pin-Namen an und gibt einen **IPin** -Zeiger zurück. Der Medientyp wird verwendet, wenn die PIN eine Verbindung mit einem anderen Filter herstellt, in der Regel ein Decoder – ein Beispiel ist der Abschnitt [mit der Demux-Datei mit elementaren Datenströmen](using-the-demux-with-elementary-streams.md). Der PIN-Name kann beliebig sein, mit dem Unterschied, dass doppelte Pin-Namen nicht zulässig sind.

Anschließend weisen Sie dem neuen Ausgabepin eine oder mehrere Datenstrom-IDs oder PIDs zu. Fragen Sie für Programmstreams die PIN nach **IMPEG2StreamIdMap** ab, und nennen Sie [**IMPEG2StreamIdMap:: mapstreamid**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid). Fragen Sie für Transportstreams die PIN für **IMPEG2PIDMap** ab, und nennen Sie [**IMPEG2PIDMap:: mappid**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid).

Es gibt mehrere Möglichkeiten, wie das-Element TS-Pakete analysieren kann. Für jede Ausgabepin wird die-Methode durch den *mediasamplecontent* -Parameter der **mappid-** Methode bestimmt.



| Wert                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Daten \_ Strom für Medien \_ | Der Filter liefert PE-Nutzlasten. In diesem Modus stellt der Filter die PE-Pakete bereit, sodass der Downstream-Filter den es-Byte-Stream ohne die PE-Paket Header empfängt. (Nur Audiodaten und Videostreams.)                                                                                                                                                     |
| Medien- \_ MPEG2 \_ PSI         | Der Filter bietet umfassende PSI-Abschnitte, wie z. b. Pat-Tabellen, PMT-Tabellen, Cat-Tabellen usw.                                                                                                                                                                                                                                                               |
| Nutzlast für Medien \_ Transport \_ | Der Filter extrahiert die Nutzlasten aus den TS-Paketen und übermittelt Sie ohne weitere Verarbeitung. Bei elementaren Datenströmen bedeutet dies, dass die-Methode vollständige PE-Pakete, einschließlich der PE-Paket Header, bereitstellt.                                                                                                                                                    |
| Medien \_ Transport \_ Paket  | Der Filter liefert ganze TS-Pakete. Die "demux" leitet die TS-Pakete entsprechend ihren PIDs weiter, untersucht oder verarbeitet die Pakete andernfalls nicht. Pakete mit Fehlern werden nicht herausgefiltert. Die Pakete werden von der Demux-Datei nicht erneut durchsucht, und der resultierende Ausgabedatenstrom ist kein kompatibler MPEG-2-Transportstream. Dieser Modus wird als *Pass-Through* -Modus bezeichnet. |



 

Bei Programmstreams übermittelt die Debug-Abteilung immer PE-Nutzlasten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



