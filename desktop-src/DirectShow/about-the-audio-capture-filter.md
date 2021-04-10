---
description: Informationen zum audioerfassungs Filter
ms.assetid: ff345670-5a75-40d3-a228-8bc22aa76708
title: Informationen zum audioerfassungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5e28bef37ca52f0a33fc95b6d2a387cbbe2fb3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125281"
---
# <a name="about-the-audio-capture-filter"></a>Informationen zum audioerfassungs Filter

DirectShow ermöglicht die Erfassung aus den analogen Eingaben auf einer Soundkarte über den [audioerfassungs Filter](audio-capture-filter.md). Dieser Filter verwendet die WaveIn *xxx* -APIs, um jedes Gerät zu steuern, dessen Treiber diese APIs unterstützt. Jede Karte im System wird durch eine separate Instanz des Filters dargestellt.

Der audioerfassungs Filter macht jede Eingabe auf der Karte (z. b. das Mikrofon oder die Eingabe-PIN) verfügbar. Die Eingabe Pins stellen dar, was der Treiber als audioquellzeilen verfügbar macht. Es werden jedoch keine Daten durch diese Eingabe Pins durchlaufen, und Sie stellen keine Verbindung mit anderen DirectShow-Filtern her. Sie bieten lediglich eine Möglichkeit für eine Anwendung, die Eingaben zu steuern. Die Anwendung kann eine Eingabe-PIN verwenden, um die Eingabe zu aktivieren oder zu deaktivieren, oder um Mischungs Eigenschaften wie z. b. Bass-Ausgleich, Höhen-Ausgleich, Pan usw. festzulegen. Der verfügbare Steuerungs Umfang hängt vom Treiber ab. Um die Funktionen einer bestimmten Soundkarte vollständig zu verstehen und auszunutzen, benötigen Sie die Dokumentation des Herstellers der Karte.

> [!Note]  
> Sie können eine Erfassung aus den CD-Audio Eingaben durchführen, aber dieser Audiostream wurde bereits über den Digital-to-Analog-Konverter durchlaufen, sodass es zu einem Verlust der Soundqualität von der ursprünglichen CD kommt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioerfassung](audio-capture.md)
</dt> </dl>

 

 



