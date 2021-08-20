---
title: Installieren von benutzerdefinierten E/A-Prozeduren
description: Installieren von benutzerdefinierten E/A-Prozeduren
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- Multimediadatei-E/A, benutzerdefinierte Prozeduren
- Datei-E/A, benutzerdefinierte Prozeduren
- Eingabe und Ausgabe (E/A), benutzerdefinierte Prozeduren
- E/A (Eingabe und Ausgabe), benutzerdefinierte Prozeduren
- Installieren von benutzerdefinierten E/A-Prozeduren
- Benutzerdefinierte E/A
- mmioInstallIOProc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ec92542efe80c24e1e620983d78b4b9a6c246ff003934a1ace1cae159fbd1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140464"
---
# <a name="installing-custom-io-procedures"></a>Installieren von benutzerdefinierten E/A-Prozeduren

So installieren Sie eine E/A-Prozedur, die zugeordnet ist. Verwenden Sie die Arc-Dateinamenerweiterung wie folgt mit der [**mmioInstallIOProc-Funktion:**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Wenn Sie eine E/A-Prozedur mit [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)installieren, bleibt die Prozedur installiert, bis Sie sie entfernen. Die E/A-Prozedur wird für jede Datei verwendet, die Sie öffnen, solange die Datei über die entsprechende Dateinamenerweiterung verfügt.

Sie können eine E/A-Prozedur auch vorübergehend installieren, indem Sie die [**mmioOpen-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) verwenden. In diesem Fall wird die E/A-Prozedur nur mit einer Datei verwendet, die mit **mmioOpen** geöffnet wurde, und wird entfernt, wenn die Datei mithilfe der [**mmioClose-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) geschlossen wird. Um beim Öffnen einer Datei mit **mmioOpen** eine E/A-Prozedur anzugeben, verwenden Sie den *lpmmioinfo-Parameter,* um wie folgt auf eine [**MMIOINFO-Struktur**](/previous-versions//dd757322(v=vs.85)) zu verweisen:

1.  Legen Sie den **fccIOProc-Member** auf **NULL** fest.
2.  Legen Sie den **pIOProc-Member** auf die Prozedurinstanzadresse der E/A-Prozedur fest.
3.  Legen Sie alle anderen Member auf 0 fest (es sei denn, Sie öffnen eine Speicherdatei oder lesen oder schreiben direkt in den Datei-E/A-Puffer).

Stellen Sie sicher, dass Sie alle E/A-Prozeduren entfernen, die Sie installiert haben, bevor Sie Ihre Anwendung beenden.

 

 