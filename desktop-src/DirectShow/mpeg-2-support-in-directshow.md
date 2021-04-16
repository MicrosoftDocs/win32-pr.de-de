---
description: MPEG-2-Unterstützung in DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: MPEG-2-Unterstützung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522195"
---
# <a name="mpeg-2-support-in-directshow"></a>MPEG-2-Unterstützung in DirectShow

In diesem Abschnitt werden die Komponenten beschrieben, die Sie verwenden können, um MPEG-2-Inhalte in DirectShow wiederzugeben.

> [!Note]  
> Obwohl DVD-Videos auf MPEG-2 basieren, wird in diesem Abschnitt weder die DVD-Wiedergabe noch die Navigation beschrieben. Weitere Informationen zu DVD in DirectShow finden Sie unter [DVD-Anwendungen](dvd-applications.md).

 

MPEG-2-Daten können aus einer lokalen Datei oder aus einer Live Quelle, z. b. einem Netzwerk Broadcast oder einem D-VHS-Gerät, stammen. Die Dateiwiedergabe wird als *Pullmodus* bezeichnet, da der Parserfilter Daten aus der Datei in das Filter Diagramm zieht. Live Quellen werden als *Pushmodus* bezeichnet, da der Quell Filterdaten per Push in das Diagramm überträgt.

DirectShow stellt zwei Filter bereit, mit denen MPEG-2-Systemdaten Ströme analysiert werden können:

-   [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): dieser Filter unterstützt den Pushmodus für Programmstreams und Transportdaten Ströme. In Windows XP und höher unterstützt es auch den Pullmodus für Programmstreams.
-   [MPEG-2-Splitter](mpeg-2-splitter.md): dieser Filter unterstützt den Pullmodus für Programmstreams auf downlevelplattformen. Dieser Filter ist in Windows XP und höher veraltet.

Wenn Sie den "MPEG-2 demux"-oder "MPEG-2"-Splitter verwenden möchten, müssen Sie über DirectShow-kompatible MPEG-2-Audiodateien und-Video-Decoder verfügen, die die in "packetisiert"-

Dieser Abschnitt enthält die folgenden Themen:

-   [Übersicht über MPEG-2-Systeme](overview-of-mpeg-2-systems.md)
-   [Verwenden von MPEG-2 Demultiplexer](using-the-mpeg-2-demultiplexer.md)
-   [Verwenden des MPEG-2-Splitters](using-the-mpeg-2-splitter.md)
-   [MPEG-Beispiel Eigenschaften](mpeg-sample-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel für PSI-Parser-Filter](psi-parser-filter-sample.md)
</dt> </dl>

 

 



