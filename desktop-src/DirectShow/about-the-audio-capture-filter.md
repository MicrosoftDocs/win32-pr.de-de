---
description: Informationen zum Audioaufnahmefilter
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Informationen zum Audioaufnahmefilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9127cd0e93e7b5aed09674474d502f16c47f03e3317e437fdea9c4f7b2d3d8b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118002431"
---
# <a name="about-the-audio-capture-filter"></a>Informationen zum Audioaufnahmefilter

DirectShow ermöglicht die Erfassung aus den analogen Eingaben auf einer Soundkarte über den [Audioaufnahmefilter](audio-capture-filter.md). Dieser Filter verwendet die waveIn XXX-APIs, um alle Geräte zu steuern, deren Treiber diese APIs unterstützt. Jede Karte im System wird durch eine separate Instanz des Filters dargestellt.

Der Filter Audio capture macht jede Eingabe auf der Karte, z. B. das Mikrofon oder die EINGABEEINGABE, als Eingabepin verfügbar. Die Eingabepins stellen dar, was der Treiber als Audioquelllinien verfügbar macht. Es werden jedoch keine Daten durch diese Eingabepins geleitet, und sie stellen keine Verbindung mit anderen DirectShow-Filtern her. Sie bieten einer Anwendung einfach die Möglichkeit, die Eingaben zu steuern. Die Anwendung kann einen Eingabepin verwenden, um die Eingabe zu aktivieren oder zu deaktivieren oder gemischte Eigenschaften wie z. B. die Gleichmäßigisierung, den Treble-Ausgleich, schwenken usw. festzulegen. Welche Steuerungsmenge verfügbar ist, hängt vom Treiber ab. Um die Funktionen einer bestimmten Soundkarte vollständig zu verstehen und zu nutzen, benötigen Sie die Dokumentation des Kartenherstellers.

> [!Note]  
> Sie können aus der CD-Audio-Eingabe erfassen, aber dieser Audiostream hat bereits den Digital-to-Analog-Konverter durchlaufen, sodass die Tonqualität der ursprünglichen CD verloren geht.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioaufnahme](audio-capture.md)
</dt> </dl>

 

 



