---
title: Datei Übertragungs Konsistenz
description: Bits gewährleistet, dass die Version der Datei, die Sie überträgt, basierend auf der Dateigröße und dem Zeitstempel und nicht auf dem Inhalt konsistent ist (Bits schützt nicht vor man-in-the-Middle-Angriffen).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855476"
---
# <a name="file-transfer-consistency"></a>Datei Übertragungs Konsistenz

Bits gewährleistet, dass die Version der Datei, die Sie überträgt, basierend auf der Dateigröße und dem Zeitstempel und nicht auf dem Inhalt konsistent ist (Bits schützt nicht vor man-in-the-Middle-Angriffen). Um den Inhalt selbst zu überprüfen, können Sie die [**IBackgroundCopyFile3:: gettemporaryname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) -Methode verwenden, um den Namen der Datei abzurufen, die den heruntergeladenen Inhalt enthält, den Inhalt mithilfe Ihres eigenen Mechanismus überprüfen und dann die [**IBackgroundCopyFile3:: setvalidationstate**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) -Methode aufrufen, um Bits anzuzeigen, wenn der Inhalt der Datei gültig ist. Wenn Sie den Überprüfungs Zustand auf **false** festgelegt haben und der Inhalt vom Ursprungsserver stammt, wechselt der Auftrag in den Fehlerzustand. Wenn der Inhalt von einem Peer stammt, lädt Bits die Datei vom Ursprungsserver herunter.

Wenn die Dateigröße oder der Zeitstempel beim Übertragen der Datei von Bits geändert wird, wird die Übertragung dieser Datei von Bits neu gestartet. Wenn der Download Auftrag z. b. zwei Dateien enthält und die Dateien auf dem Server aktualisiert werden, während Bits die zweite Datei überträgt, wird die Übertragung der zweiten Datei von Bits neu gestartet. Die erste Datei, die bereits erfolgreich übertragen wurde, wird nicht aktualisiert, um die neuen Änderungen widerzuspiegeln.

Beachten Sie Folgendes: Wenn Sie der Besitzer der Datei sind, die vom Server heruntergeladen wird, sollten Sie eine neue URL für jede neue Version der Datei erstellen. Wenn Sie die gleiche URL für neue Versionen der Datei verwenden, können einige Proxy Server veraltete Daten aus Ihrem Cache verarbeiten, da Sie nicht mit dem ursprünglichen Server überprüft werden, wenn die Datei veraltet ist.

Wenn bei Uploads die Dateigröße oder der Zeitstempel während der Dateiübertragung geändert wird, generiert Bits einen Fehler, und der Auftrag wird in den Status Fehler des Status "BG- \_ Auftragsstatus" versetzt \_ \_ .

Bits synchronisiert keine Übertragungsanforderungen, wenn mindestens ein Benutzer anfordert, dass dieselbe Datei an denselben Speicherort übertragen wird. Bits überträgt die Datei für jede Anforderung separat.

 

 




