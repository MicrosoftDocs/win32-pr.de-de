---
description: Senden von COPP-Befehlen
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Senden von COPP-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044756f8bdfe59e44309c158cb0be1dc983143d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345393"
---
# <a name="sending-copp-commands"></a>Senden von COPP-Befehlen

Um einen zertifizierten Befehl für das Ausgabe Schutz Protokoll (COPP) zu senden, füllen Sie die [**amcoppcommand**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) -Struktur wie folgt aus:

-   **guidcommandid**. Die GUID, die den Befehl identifiziert. Weitere Informationen finden Sie in der COPP-Befehlsreferenz.
-   **dwsequence**. Die Sequenznummer des Befehls. Erhöhen Sie diesen Wert nach jedem Befehl. (Dieser Wert wird als **ucommandabq** in [Initiieren einer COPP-Sitzung](initiating-a-copp-session.md)angezeigt.)
-   **cbsizedata**. Die Größe (in Bytes) der Daten, die für den Befehl erforderlich sind.
-   **Commanddata**. Daten für den Befehl.

Nachdem Sie diese Daten ausgefüllt haben, berechnen Sie den Mac für den Befehl:

1.  Berechnen Sie das OMAC-1-Tag für den Datenblock, der nach dem **mackdi** -Member der **amcoppcommand** -Struktur angezeigt wird.
2.  Kopieren Sie diesen Wert in den **mackdi** -Member der-Struktur.

Übergeben Sie nun die Struktur an die [**iamcertifiedoutputprotection::P rotectioncommand**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand) -Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



