---
title: Ändern der Sequencer-Synchronisierung
description: Ändern der Sequencer-Synchronisierung
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET Befehls Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bffdc1606624f63fa05a9cc03c68fe64781620f
ms.sourcegitcommit: 8276af9231bdbf5a7334299f0d13fc8ff069a065
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/12/2021
ms.locfileid: "106367252"
---
# <a name="changing-sequencer-synchronization"></a>Ändern der Sequencer-Synchronisierung

> [!NOTE]
> Bias-freie Kommunikation Microsoft unterstützt eine unterschiedlichste und inklusive Umgebung.  In diesem Dokument sind Verweise auf das Wort "Slave" vorhanden. Im [Stil Handbuch von Microsoft für die Bias-Free-Kommunikation](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) wird dies als ausschließendes Wort erkannt.  Dieser Wortlaut wird verwendet, da es sich zurzeit um den in der Software verwendeten Wortlaut handelt. Aus Konsistenz Gründen enthält dieses Dokument dieses Wort. Wenn dieses Wort aus der Software entfernt wird, korrigieren wir dieses Dokument als Ausrichtung.

Um den Synchronisierungs Modus eines Sequencer-Geräts zu ändern, verwenden Sie die [**MCI \_ set**](mci-set.md) -Befehls Meldung mit den MCI \_ Seq \_ Set \_ Master-und MCI \_ Seq \_ Set \_ Slave-Flags. Zwei Member in der [**MCI \_ Seq \_ Set- \_ Parametern**](mci-seq-set-parms.md) -Struktur, **dwmaster** und **dwslave**, werden verwendet, um den Master-und den untergeordneten Synchronisierungs Modus anzugeben.

Der Master Synchronisierungs Modus steuert die vom Sequencer gesendeten Synchronisierungs Informationen an einen Ausgabeport. Im folgenden finden Sie die Konstanten für den **dwmaster** -Member und die entsprechenden Master Synchronisierungs Modi.



| Konstante        | Synchronisierungsmodus                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ -Integration \_  | MIDI-Synchronisierung. Senden von Zeit Steuerungsinformationen an den Ausgabeport mithilfe von MIDI-Zeitachsen Nachrichten   |
| MCI- \_ \_ SMPTE | SMPTE-Synchronisierung. Senden von Zeit Steuerungsinformationen an den Ausgabeport mithilfe von Nachrichten im Rahmen von MIDI |
| MCI-nicht verfügbar \_ \_  | Keine Synchronisierung. Senden Sie keine Zeit Steuerungsinformationen.                                                  |



 

Der untergeordnete Synchronisierungs Modus steuert, wo der Sequencer seine Zeit Steuerungsinformationen für die Wiedergabe einer MIDI-Datei abruft. Im folgenden finden Sie die Konstanten für den **dwslave** -Member und die entsprechenden untergeordneten Synchronisierungs Modi.



| Konstante        | Synchronisierungsmodus                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| MCI- \_ \_ Datei  | Datei Synchronisierung. Zeit Steuerungsinformationen aus der MIDI-Datei erhalten.                                                                                       |
| MCI \_ -Integration \_  | MIDI-Synchronisierung. Informationen zur zeitlichen Steuerung aus dem eingabeport mithilfe von MIDI-Zeitachsen Nachrichten                                                     |
| MCI- \_ \_ SMPTE | SMPTE-Synchronisierung. Informationen zur zeitlichen Steuerung aus dem eingabeport mithilfe von MIDI-Quartals Frame-Nachrichten                                                   |
| MCI-nicht verfügbar \_ \_  | Keine Synchronisierung. Erhalten Sie nur Zeit Steuerungsinformationen von MCI-Befehlen, und ignorieren Sie Zeit Steuerungsinformationen (z. b. die Änderung von Änderungen) in der Datei "MIDI" |



 

> [!Note]  
> Derzeit unterstützt der MCI-Dienst für die Master Synchronisierung nur den Modus "keine Synchronisierung" (MCI-"keine" \_ \_ ). Bei der untergeordneten Synchronisierung wird nur der Datei Synchronisierungs Modus (MCI \_ \_ -Datei) und der Modus "keine Synchronisierung" (MCI-Datei "keine") unterstützt \_ \_ .

 

 

 




