---
description: MPEG-2-Unterstützung in DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: MPEG-2-Unterstützung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9feaa24ea36b6f5e00e0f6ecd5db49ce37181f9d6d7348b3cfa27e64f7f2d84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075800"
---
# <a name="mpeg-2-support-in-directshow"></a>MPEG-2-Unterstützung in DirectShow

In diesem Abschnitt werden die Komponenten beschrieben, die Sie zum Wiedergeben von MPEG-2-Inhalten in DirectShow verwenden können.

> [!Note]  
> Obwohl DVD-Video auf MPEG-2 basiert, beschreibt dieser Abschnitt die DVD-Wiedergabe oder -Navigation nicht. Informationen zur DVD in DirectShow finden Sie unter [DVD-Anwendungen.](dvd-applications.md)

 

MPEG-2-Daten können aus einer lokalen Datei oder aus einer Livequelle wie einer Netzwerkübertragung oder einem D-VHS-Gerät stammen. Die Dateiwiedergabe wird als *Pullmodus* bezeichnet, da der Parserfilter Daten aus der Datei in das Filterdiagramm abruft. Livequellen werden als *Pushmodus* bezeichnet, da der Quellfilter Daten in das Diagramm pusht.

DirectShow bietet zwei Filter, die MPEG-2-Systemstreams analysieren können:

-   [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): Dieser Filter unterstützt den Pushmodus für Programm- und Transportstreams. In Windows XP und höher wird auch der Pullmodus für Programmstreams unterstützt.
-   [MPEG-2-Splitter:](mpeg-2-splitter.md)Dieser Filter unterstützt den Pullmodus für Programmstreams auf downleveln Plattformen. Dieser Filter ist in Windows XP und höher veraltet.

Um den MPEG-2-Demux- oder MPEG-2-Splitter zu verwenden, benötigen Sie DirectShow-kompatible MPEG-2-Audio- und Videodecoder, die paketisierte elementare Streams (PES) akzeptieren.

Dieser Abschnitt enthält die folgenden Themen:

-   [Übersicht über MPEG-2-Systeme](overview-of-mpeg-2-systems.md)
-   [Verwenden des MPEG-2-Demultiplexers](using-the-mpeg-2-demultiplexer.md)
-   [Verwenden des MPEG-2-Splitters](using-the-mpeg-2-splitter.md)
-   [MPEG-Beispieleigenschaften](mpeg-sample-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PSI Parser-Filterbeispiel](psi-parser-filter-sample.md)
</dt> </dl>

 

 



