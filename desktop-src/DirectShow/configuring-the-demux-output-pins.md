---
description: Konfigurieren der Demux-Ausgabepins
ms.assetid: c53f3fe6-5588-4faf-ba5c-6a6cf7e16f3a
title: Konfigurieren der Demux-Ausgabepins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0456b7354c23048bafe012439d5d2c4fa1843df601ee2d8e49aa62dfc01a4b9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813610"
---
# <a name="configuring-the-demux-output-pins"></a>Konfigurieren der Demux-Ausgabepins

Wenn der MPEG-2-Demux ein Datenpaket empfängt, muss er bestimmen, welcher Ausgabepin die Daten analysieren und ausliefern soll. Im Programmstreammodus ordnet demux Stream-IDs Ausgabepins zu. Im Transportstreammodus ordnet er PIDs Ausgabepins zu. Wenn z. B. im Transportstreammodus pid 0x31 Pin 0 zugeordnet ist, wird jedes TS-Paket mit dieser PID-Nummer an den Ausgabepin 0 geroutet. Wenn der Demux ein Paket empfängt, dessen Datenstrom-ID oder PID keinen Ausgabepins zugeordnet ist, verwirft es einfach das Paket.

Im Pullmodus erstellt der Demux automatisch Ausgabepins für die Audio- und Videostreams in der Datei und ordnet die Stream-IDs den Pins zu.

Im Pushmodus müssen die Ausgabepins von der Anwendung oder einem anderen Filter konfiguriert werden. Bei digitalen Fernsehquellen, die die Broadcasttreiberarchitektur (Broadcast Driver Architecture, BDA) verwenden, arbeitet der Netzwerkanbieterfilter mit dem TIF-Filter zusammen, um die Demux zu konfigurieren. Die Anwendung muss nichts tun. In anderen Szenarien muss die Anwendung die Ausgabepins konfigurieren.

Der Demux beginnt ohne Ausgabepins. Um einen Ausgabepin zu erstellen, rufen Sie die [**IMpeg2Demultiplexer::CreateOutputPin-Methode**](/windows/desktop/api/Strmif/nf-strmif-impeg2demultiplexer-createoutputpin) für den Filter auf. Diese Methode verwendet einen Medientyp und einen Pinnamen und gibt einen **IPin-Zeiger** zurück. Der Medientyp wird verwendet, wenn die Stecknadel eine Verbindung mit einem anderen Filter herstellt, in der Regel mit einem Decoder. Ein Beispiel hierfür ist der Abschnitt [Using the Demux with Elementary Streams.](using-the-demux-with-elementary-streams.md) Der Pinname kann einen anderen Namen haben, mit der Ausnahme, dass doppelte Pinnamen nicht zulässig sind.

Weisen Sie als Nächstes dem neuen Ausgabepin eine oder mehrere Stream-IDs oder PIDs zu. Fragen Sie für Programmstreams den Pin nach **IMPEG2StreamIdMap** ab, und rufen [**Sie IMPEG2StreamIdMap::MapStreamId auf.**](/windows/desktop/api/Strmif/nf-strmif-impeg2streamidmap-mapstreamid) Fragen Sie für Transportstreams den Pin nach **IMPEG2PIDMap** ab, und rufen [**Sie IMPEG2PIDMap::MapPID auf.**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid)

Es gibt mehrere Möglichkeiten, wie der Demux TS-Pakete analysieren kann. Für jeden Ausgabepin wird die Analysemethode durch den *MediaSampleContent-Parameter* für die **MapPID-Methode** bestimmt.



| Wert                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MEDIA \_ ELEMENTARY \_ STREAM | Der Filter liefert PES-Nutzlasten. In diesem Modus entpackt der Filter die PES-Pakete, sodass der Downstreamfilter den ES-Bytestream ohne die PES-Paketheader empfängt. (Nur Audio- und Videostreams.)                                                                                                                                                     |
| MEDIA \_ MPEG2 \_ PSI         | Der Filter stellt vollständige PSI-Abschnitte wie PAT-Tabellen, PMT-Tabellen, CAT-Tabellen usw. zur Verfügung.                                                                                                                                                                                                                                                               |
| \_ \_ MEDIENTRANSPORTNUTZLAST | Der Filter extrahiert die Nutzlasten aus den TS-Paketen und liefert sie ohne weitere Analyse. Bei elementaren Streams bedeutet dies, dass der Demux ganze PES-Pakete einschließlich der PES-Paketheader liefert.                                                                                                                                                    |
| \_ \_ MEDIENTRANSPORTPAKET  | Der Filter liefert vollständige TS-Pakete. Der Demux leitet die TS-Pakete gemäß ihren PIDs weiter, untersucht oder verarbeiten die Pakete jedoch nicht anderweitig. Pakete mit Fehlern werden nicht herausgefiltert. Die Demux-Datei multiplext die Pakete nicht erneut, und der resultierende Ausgabestream ist kein konformer MPEG-2-Transportstream. Dieser Modus wird als *Pass-Through-Modus* bezeichnet. |



 

Für Programmstreams stellt die Demux immer PES-Nutzlasten zur Anwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des MPEG-2-Demultiplexers](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



