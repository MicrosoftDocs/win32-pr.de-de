---
title: Treiberunterstützung für MCI-Befehle
description: Treiberunterstützung für MCI-Befehle
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709587"
---
# <a name="driver-support-for-mci-commands"></a>Treiberunterstützung für MCI-Befehle

MCI-Treiber stellen die Funktionalität für MCI-Befehle bereit. Die Systemsoftware führt einige grundlegende Daten Verwaltungsaufgaben aus, aber die gesamte Multimedia-Wiedergabe,-Präsentation und-Aufzeichnung wird von den einzelnen MCI-Treibern verarbeitet.

Treiber unterscheiden sich in der Unterstützung von MCI-Befehlen und Befehlsflags. Da Multimedia-Geräte vielfältige Funktionen haben können, ist MCI so konzipiert, dass einzelne Treiber die Befehls Sätze erweitern oder reduzieren können, damit Sie den Funktionen des Geräts entsprechen. Der [**Datensatz**](record.md) -Befehl ([**MCI- \_ Datensatz**](mci-record.md)) ist z. b. Teil des Befehlssatzes für MIDI-Sequencer, aber der in Windows enthaltene mciseq-Treiber unterstützt diesen Befehl nicht. Das Referenz Thema für den Datensatz-Befehl erläutert, dass Geräte des **Sequencer** -Gerätetyps den Befehl erkennen. Dies bedeutet nicht, dass alle Geräte dieses Typs den Befehl unterstützen. Anwendungen [**sollten den Funktionsbefehl**](capability.md) ([**MCI \_ getdevcaps**](mci-getdevcaps.md)) verwenden, um die Funktionen eines bestimmten Geräts zu bestimmen.

 

 




