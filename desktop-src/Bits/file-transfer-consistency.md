---
title: Dateiübertragungskonsistenz
description: BITS garantiert, dass die version der übertragenen Datei basierend auf der Dateigröße und dem Zeitstempel konsistent ist, nicht auf Inhalt (BITS schützt nicht vor Man-in-the-Middle-Angriffen).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608566f6e9927fdcb39133c30720a46ead869f36d3084c950b9ed86379c4b749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959499"
---
# <a name="file-transfer-consistency"></a>Dateiübertragungskonsistenz

BITS garantiert, dass die version der übertragenen Datei basierend auf der Dateigröße und dem Zeitstempel konsistent ist, nicht auf Inhalt (BITS schützt nicht vor Man-in-the-Middle-Angriffen). Um den Inhalt selbst zu überprüfen, können Sie die [**IBackgroundCopyFile3::GetTemporaryName-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) verwenden, um den Namen der Datei abzurufen, die den heruntergeladenen Inhalt enthält, den Inhalt mithilfe Ihres eigenen Mechanismus zu überprüfen, und dann die [**IBackgroundCopyFile3::SetValidationState-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) aufrufen, um BITS anzugeben, ob der Inhalt der Datei gültig ist. Wenn Sie den Überprüfungszustand auf **FALSE** festlegen und der Inhalt vom Ursprungsserver stammt, wechselt der Auftrag in den Fehlerzustand. Wenn der Inhalt von einem Peer stammt, lädt BITS die Datei vom Ursprungsserver herunter.

Wenn sich bei Downloads die Dateigröße oder der Zeitstempel ändert, während BITS die Datei überträgt, startet BITS nur die Übertragung dieser Datei neu. Wenn der Downloadauftrag beispielsweise zwei Dateien enthält und die Dateien auf dem Server aktualisiert werden, während BITS die zweite Datei überträgt, startet BITS nur die Übertragung der zweiten Datei neu. Die erste Datei, die bereits erfolgreich übertragen wurde, wird nicht aktualisiert, um die neuen Änderungen widerzuspiegeln.

Beachten Sie Folgendes: Wenn Sie der Eigentümer der Datei sind, die vom Server heruntergeladen wird, sollten Sie eine neue URL für jede neue Version der Datei erstellen. Wenn Sie dieselbe URL für neue Versionen der Datei verwenden, können einige Proxyserver veraltete Daten aus dem Cache bereitstellen, da sie nicht mit dem ursprünglichen Server überprüfen, ob die Datei veraltet ist.

Wenn sich bei Uploads die Dateigröße oder der Zeitstempel während der Dateiübertragung ändert, generiert BITS einen Fehler, und der Auftrag wird in den Status BG \_ JOB \_ STATE ERROR \_ versetzt.

BITS synchronisiert keine Übertragungsanforderungen, wenn ein oder mehrere Benutzer anfordern, dass dieselbe Datei an denselben Speicherort übertragen wird. BITS überträgt die Datei für jede Anforderung separat.

 

 




