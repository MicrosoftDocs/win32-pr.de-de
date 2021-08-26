---
description: Senden von COPP-Befehlen
ms.assetid: aba0bd34-f5bb-4233-bde2-0dfd8f1ff0bf
title: Senden von COPP-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66a6ad66abe7e6c4a596446b147fe5943c5460b4ef540dbc5e5a3dfad4bdc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078880"
---
# <a name="sending-copp-commands"></a>Senden von COPP-Befehlen

Um einen COPP-Befehl (Certified Output Protection Protocol) zu senden, geben Sie eine [**AMCOPPCommand-Struktur**](/windows/win32/api/strmif/ns-strmif-amcoppcommand) wie folgt ein:

-   **guidCommandID**. Die GUID, die den Befehl identifiziert. Weitere Informationen finden Sie in der COPP-Befehlsreferenz.
-   **dwSequence**. Die Sequenznummer des Befehls. Erhöhen Sie diesen Wert nach jedem Befehl. (Dieser Wert wird unter Initiieren einer [COPP-Sitzung](initiating-a-copp-session.md)als **uCommandSeq** angezeigt.)
-   **cbSizeData**. Die Größe aller für den Befehl benötigten Daten in Bytes.
-   **CommandData**. Daten für den Befehl.

Nachdem Sie diese Daten ausgefüllt haben, berechnen Sie den MAC für den Befehl:

1.  Berechnen Sie das OMAC-1-Tag für den Datenblock, der nach dem **macKDI-Member** der **AMCOPPCommand-Struktur** angezeigt wird.
2.  Kopieren Sie diesen Wert in den **macKDI-Member** der -Struktur.

Übergeben Sie nun die -Struktur an die [**IAMCertifiedOutputProtection::P rotectionCommand-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectioncommand)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



