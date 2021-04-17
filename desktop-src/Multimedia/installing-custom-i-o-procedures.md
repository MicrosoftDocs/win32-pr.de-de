---
title: Installieren benutzerdefinierter e/a-Prozeduren
description: Installieren benutzerdefinierter e/a-Prozeduren
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- Multimedia-Datei-e/a, benutzerdefinierte Verfahren
- Datei-e/a, benutzerdefinierte Prozeduren
- Eingabe und Ausgabe (e/a), benutzerdefinierte Prozeduren
- E/a (Eingabe und Ausgabe), benutzerdefinierte Prozeduren
- Installieren benutzerdefinierter e/a-Prozeduren
- benutzerdefinierte e/a
- mmioinstallioproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390307"
---
# <a name="installing-custom-io-procedures"></a>Installieren benutzerdefinierter e/a-Prozeduren

Zum Installieren einer e/a-Prozedur, die dem zugeordnet ist. Dateinamenerweiterung des Bogens, verwenden Sie die [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) -Funktion wie folgt:


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Wenn Sie eine e/a-Prozedur mit [**mmioinstallioproc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)installieren, bleibt die Prozedur installiert, bis Sie Sie entfernen. Die e/a-Prozedur wird für jede Datei verwendet, die Sie öffnen, solange die Datei über die entsprechende Dateierweiterung verfügt.

Sie können auch eine e/a-Prozedur vorübergehend mithilfe der [**mmioopen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) -Funktion installieren. In diesem Fall wird die e/a-Prozedur nur mit einer Datei verwendet, die mit **mmioopen** geöffnet wurde, und wird entfernt, wenn die Datei mit der [**mmioclose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) -Funktion geschlossen wird. Verwenden Sie zum Angeben einer e/a-Prozedur, wenn Sie eine Datei mit **mmioopen** öffnen, den *lpmmioinfo* -Parameter wie folgt, um auf eine [**mmioinfo**](/previous-versions//dd757322(v=vs.85)) -Struktur zu verweisen:

1.  Legen Sie den **fccioproc** -Member auf **null** fest.
2.  Legen Sie den **pioproc** -Member auf die Prozedur Instanz-Adresse des e/a-Verfahrens fest.
3.  Legen Sie alle anderen Mitglieder auf 0 (null) fest (es sei denn, Sie öffnen eine Speicherdatei oder lesen oder schreiben direkt in den Datei-e/a-Puffer).

Entfernen Sie alle e/a-Prozeduren, die Sie installiert haben, bevor Sie die Anwendung beenden.

 

 