---
title: Funktionen und Strukturen des Audiokomprimierungs-Managers
description: Funktionen und Strukturen des Audiokomprimierungs-Managers
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- Multimediaaudio, ACM-Funktionen
- Audio,ACM-Funktionen
- Audiokomprimierungs-Manager (ACM), Funktionen
- ACM (Audiokomprimierungs-Manager), Funktionen
- Multimediaaudio, ACM-Strukturen
- Audio, ACM-Strukturen
- Audiokomprimierungs-Manager (ACM), Strukturen
- ACM (Audiokomprimierungs-Manager), Strukturen
- ACM-Strukturen
- ACM-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabd9a66bee13c02c87df95565744eb973283baedb7e955449feb2ddad3005a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808380"
---
# <a name="audio-compression-manager-functions-and-structures"></a>Funktionen und Strukturen des Audiokomprimierungs-Managers

Die ACM-Funktionen lassen sich in verschiedene Kategorien unterteilen. Namenskonventionen für die Funktionen machen es einfach, diese Kategorien zu identifizieren. Funktionsnamen (mit zwei Ausnahmen) haben die Form *acmGroupFunction,* wobei *Group* die ACM-Kategorie bestimmt (z.B. "Driver", "Format", "FormatTag", "Filter", "FilterTag" oder "Stream"), und *Function* beschreibt die von der Funktion ausgeführte Aktion.

Die Funktionen in den Filter- und Formatgruppen sind sehr ähnlich. Fast jede Funktion, die auf Filtern arbeitet, verfügt über eine parallele Funktion, die auf Formaten arbeitet.

In der Formatgruppe verwenden einige Funktionen Waveform-Audio-Formattags **(das wFormatTag-Member** einer [**WAVEFORMATEX-Struktur),**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) während andere vollständige Waveform-Audioformate (die vollständige **WAVEFORMATEX-Struktur)** erfordern. (Referenzinformationen zur **WAVEFORMATEX-Struktur** finden Sie unter [Fehler](error.md).)

In der Filtergruppe verwenden einige Funktionen Waveform-Audio-Filtertags **(das dwFilterTag-Mitglied** einer [**WAVEFILTER-Struktur),**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) während andere vollständige Waveform-Audiofilter (die vollständige **WAVEFILTER-Struktur)** erfordern.

Die Funktionen in der Streamgruppe stellen die vielen Schritte dar, die an einer Konvertierung beteiligt sind: Öffnen einer Konvertierungsinstanz, Vorbereiten der Konvertierung, Durchführen der Konvertierung, Bereinigen nach Abschluss der Konvertierung und Schließen der Konvertierungsinstanz.

 

 