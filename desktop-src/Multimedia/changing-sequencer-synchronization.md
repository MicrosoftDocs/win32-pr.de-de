---
title: Ändern der Sequencersynchronisierung
description: Ändern der Sequencersynchronisierung
ms.assetid: 5c3acb47-e6cc-4957-a306-7039ec110827
keywords:
- MCI_SET Befehlsmeldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f7f31544b7b9ceb00109551718b9984dd2aa506557848e0d63e77724c4be32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526420"
---
# <a name="changing-sequencer-synchronization"></a>Ändern der Sequencersynchronisierung

> [!NOTE]
> Bias-free Communication Microsoft unterstützt eine vielfältige und inklusionsbasierte Umgebung.  In diesem Dokument gibt es Verweise auf das Wort "slave". Microsoft Style [Guide for Bias-Free Communications](https://github.com/MicrosoftDocs/microsoft-style-guide/blob/master/styleguide/bias-free-communication.md) erkennt dies als Ausschlusswort.  Diese Formulierung wird verwendet, da sie derzeit in der Software verwendet wird. Zur Konsistenz enthält dieses Dokument dieses Wort. Wenn dieses Wort aus der Software entfernt wird, korrigieren wir dieses Dokument so, dass es ausgerichtet ist.

Um den Synchronisierungsmodus eines Sequencergeräts zu ändern, verwenden Sie die [**MCI \_ SET-Befehlsmeldung**](mci-set.md) mit den Flags MCI SEQ SET MASTER und \_ \_ \_ MCI \_ SEQ SET \_ \_ SLAVE. Zwei Member in der [**MCI \_ SEQ \_ SET \_ PARMS-Struktur,**](mci-seq-set-parms.md) **dwMaster** und **dwSklave,** werden verwendet, um den Master- und den untergeordneten Synchronisierungsmodus anzugeben.

Der Mastersynchronisierungsmodus steuert Synchronisierungsinformationen, die vom Sequencer an einen Ausgabeport gesendet werden. Im Folgenden finden Sie die Konstanten für **das dwMaster-Mitglied** und die entsprechenden Mastersynchronisierungsmodi.



| Konstante        | Synchronisierungsmodus                                                                             |
|-----------------|--------------------------------------------------------------------------------------------------|
| MCI \_ \_ SEQQS  | SKRIPT-Synchronisierung. Senden von Zeitsteuerungsinformationen an den Ausgabeport mithilfe von ZEITGEBER-Zeitsteuerungsmeldungen.   |
| MCI \_ SEQ \_ SMPTE | SMPTE-Synchronisierung. Senden von Zeitsteuerungsinformationen an den Ausgabeport mithilfe von SIGNAL-Quarterframe-Nachrichten. |
| MCI \_ SEQ \_ NONE  | Keine Synchronisierung. Senden Sie keine Zeitsteuerungsinformationen.                                                  |



 

Der untergeordnete Synchronisierungsmodus steuert, wo der Sequencer seine Zeitsteuerungsinformationen erhält, um eine RATES-Datei wiedergeben zu können. Im Folgenden finden Sie die Konstanten für **das dwSklave-Mitglied** und die entsprechenden untergeordneten Synchronisierungsmodi.



| Konstante        | Synchronisierungsmodus                                                                                                                               |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| \_MCI-SEQ-DATEI \_  | Dateisynchronisierung. Hier erhalten Sie Zeitsteuerungsinformationen aus der DATEI DES -Dateiservers.                                                                                       |
| MCI \_ \_ SEQQS  | SKRIPT-Synchronisierung. Hier erhalten Sie Zeitsteuerungsinformationen vom Eingabeport mithilfe von ZEITGEBER-Zeitsteuerungsmeldungen.                                                     |
| MCI \_ SEQ \_ SMPTE | SMPTE-Synchronisierung. Hier erhalten Sie Zeitsteuerungsinformationen vom Eingabeport mithilfe von NACHRICHTEN im Rahmen des QUARTER-Rahmens.                                                   |
| MCI \_ SEQ \_ NONE  | Keine Synchronisierung. Sie können Nur Zeitsteuerungsinformationen von MCI-Befehlen erhalten und Zeitsteuerungsinformationen (z. B. Tempoänderungen) ignorieren, die sich in der DATEI MIT DER DATEI befinden. |



 

> [!Note]  
> Derzeit unterstützt der MCI-SEQUENCEr für die Mastersynchronisierung nur den Modus Keine Synchronisierung (MCI \_ SEQ \_ NONE). Für die untergeordnete Synchronisierung werden nur der Dateisynchronisierungsmodus (MCI SEQ FILE) und der Modus Keine Synchronisierung \_ \_ (MCI \_ SEQ \_ NONE) unterstützt.

 

 

 




