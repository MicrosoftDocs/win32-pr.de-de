---
title: Suchen nach einem subblock
description: Suchen nach einem subblock
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- Multimedia-Datei-e/a, suchen nach einem Riff Block
- Datei-e/a, suchen nach einem Riff Block
- Eingabe und Ausgabe (e/a), suchen nach einem Riff Block
- E/a (Eingabe und Ausgabe), suchen nach einem Riff Block
- Suchen nach einem Riff Block
- Format der Ressourcenaustausch Datei (Riff)
- Riff (Ressourcenaustausch-Dateiformat)
- Riff-e/a
- Riff Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d6cfb0ecc3223f4a883998e9f192bfbbb5ff276
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315111"
---
# <a name="searching-for-a-subchunk"></a>Suchen nach einem subblock

Im folgenden Beispiel wird die [**mmioabstieg**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) -Funktion verwendet, um nach dem "fmt"-Block im Abschnitt "Riff" des vorherigen Beispiels zu suchen.


```C++
// Find the format chunk (form type "FMT"); it should be 
// a subchunk of the "RIFF" parent chunk. 
mmckinfoSubchunk.ckid = mmioFOURCC('f', 'm', 't', ' '); 
if (mmioDescend(hmmio, &mmckinfoSubchunk, &mmckinfoParent, 
    MMIO_FINDCHUNK)) 
    // Error, cannot find the "FMT" chunk. 
else 
    // "FMT" chunk found. 
```



Um nach einem subblock (d. h. einem beliebigen Block, der kein "Riff" oder "List"-Block ist) zu suchen, identifizieren Sie seinen übergeordneten Block im *lpckparent* -Parameter der [**mmiodescen-**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) Funktion.

Wenn Sie keinen übergeordneten Block angeben, sollte sich die aktuelle Dateiposition am Anfang eines Segments befinden, bevor Sie die **mmiodescen-** Funktion aufruft. Wenn Sie einen übergeordneten Block angeben, kann die aktuelle Dateiposition an einer beliebigen Stelle in diesem Segment liegen.

Wenn bei der Suche nach einem subblock ein Fehler auftritt, ist die aktuelle Dateiposition nicht definiert. Sie können die [**mmioseek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) -Funktion und den **dwdataoffset** -Member der [**mmckinfo**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) -Struktur verwenden, die den übergeordneten Block beschreibt, um zum Anfang des übergeordneten Blocks zurückzukehren, wie im folgenden Beispiel gezeigt:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Da **dwdataoffset** den Offset bis zum Anfang des Daten Teils des Blocks angibt, müssen Sie 4 Bytes nach dem **dwdataoffset** suchen, um die Dateiposition nach dem Formulartyp festzulegen.

 

 