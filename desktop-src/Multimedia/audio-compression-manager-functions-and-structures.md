---
title: Funktionen und Strukturen des Audiokomprimierungs-Managers
description: Funktionen und Strukturen des Audiokomprimierungs-Managers
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- Multimedia-Audiofunktionen, ACM-Funktionen
- Audiofunktionen, ACM-Funktionen
- Audiokomprimierungs-Manager (ACM), Funktionen
- ACM (Audiokomprimierungs-Manager), Funktionen
- Multimedia-Audiodaten, ACM-Strukturen
- Audiodaten, ACM-Strukturen
- Audiokomprimierungs-Manager (ACM), Strukturen
- ACM (Audiokomprimierungs-Manager), Strukturen
- ACM-Strukturen
- ACM-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339055"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funktionen und Strukturen des Audiokomprimierungs-Managers

Die ACM-Funktionen sind in verschiedene Kategorien unterteilt. Benennungs Konventionen für die-Funktionen erleichtern die Identifizierung dieser Kategorien. Funktionsnamen (mit zwei Ausnahmen) weisen die Form *acmgroupfunction* auf, wobei die *Gruppe* die ACM-Kategorie festlegt (z. b. "Driver", "Format", "Formattag", "Filter", "Filtertag" oder "Stream") und die *Funktion* die von der Funktion ausgeführte Aktion beschreibt.

Die Funktionen in den Filter-und Format Gruppen sind sehr ähnlich. Fast jede Funktion, die auf Filter angewendet wird, verfügt über eine parallele Funktion, die für Formate fungiert.

In der Format Gruppe verwenden einige Funktionen wellenformat-Audiotags (das **wformattag** -Element einer [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur), während andere die vollständigen wellenformat-Audioformate (die vollständige **WaveFormatEx** -Struktur) benötigen. (Referenzinformationen zur **WaveFormatEx** -Struktur finden Sie unter [Error](error.md).)

In der Filter Gruppe verwenden einige Funktionen Waveform-audiofiltertags (das **dwfiltertag** -Element einer [**wavefilter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) -Struktur), während andere die vollständigen Wellenform-Audiofilter (die vollständige **Wellen Filter** Struktur) erfordern.

Die Funktionen in der streamgruppe stellen die vielen Schritte dar, die an einer Konvertierung beteiligt sind: das Öffnen einer Konvertierungs Instanz, das Vorbereiten der Konvertierung, das Ausführen der Konvertierung, das Bereinigen nach Abschluss der Konvertierung und das Schließen der Konvertierungs Instanz.

 

 