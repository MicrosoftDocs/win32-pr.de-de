---
title: Konsistenz der Dateiübertragung
description: BITS garantiert, dass die Version der Datei, die sie überträgt, basierend auf der Dateigröße und dem Zeitstempel konsistent ist und nicht auf Inhalt (BITS schützt nicht vor Man-in-the-Middle-Angriffen).
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
# <a name="file-transfer-consistency"></a>Konsistenz der Dateiübertragung

BITS garantiert, dass die Version der Datei, die sie überträgt, basierend auf der Dateigröße und dem Zeitstempel konsistent ist und nicht auf Inhalt (BITS schützt nicht vor Man-in-the-Middle-Angriffen). Um den Inhalt selbst zu überprüfen, können Sie die [**IBackgroundCopyFile3::GetTemporaryName-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) verwenden, um den Namen der Datei mit dem heruntergeladenen Inhalt zu erhalten, den Inhalt mitHilfe Ihres eigenen Mechanismus zu überprüfen und dann die [**IBackgroundCopyFile3::SetValidationState-Methode**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) auf bits zu überprüfen, wenn der Inhalt der Datei gültig ist. Wenn Sie den Überprüfungsstatus auf **FALSE festlegen** und der Inhalt vom Ursprungsserver stammt, geht der Auftrag in den Fehlerzustand über. Wenn der Inhalt von einem Peer stammt, lädt BITS die Datei vom Ursprungsserver herunter.

Wenn sich bei Downloads die Dateigröße oder der Zeitstempel ändert, während BITS die Datei überträgt, startet BITS nur die Übertragung dieser Datei neu. Wenn der Downloadauftrag beispielsweise zwei Dateien enthält und die Dateien auf dem Server aktualisiert werden, während BITS die zweite Datei überträgt, startet BITS nur die Übertragung der zweiten Datei neu. Die erste Datei, die bereits erfolgreich übertragen wurde, wird nicht aktualisiert, um die neuen Änderungen widerzu spiegeln.

Beachten Sie Folgendes: Wenn Sie die Datei besitzen, die vom Server heruntergeladen wird, sollten Sie für jede neue Version der Datei eine neue URL erstellen. Wenn Sie dieselbe URL für neue Versionen der Datei verwenden, können einige Proxyserver veraltete Daten aus ihrem Cache bereitstellen, da sie nicht mit dem ursprünglichen Server überprüfen, ob die Datei veraltet ist.

Wenn sich bei Uploads die Dateigröße oder der Zeitstempel während der Dateiübertragung ändert, generiert BITS einen Fehler, und der Auftrag wird in den Status BG \_ JOB \_ STATE ERROR \_ gesetzt.

BITS synchronisiert keine Übertragungsanforderungen, wenn ein oder mehrere Benutzer anfordern, dass dieselbe Datei an denselben Speicherort übertragen wird. BITS überträgt die Datei für jede Anforderung separat.

 

 




