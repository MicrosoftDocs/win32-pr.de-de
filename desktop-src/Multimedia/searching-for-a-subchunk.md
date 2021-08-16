---
title: Suchen nach einem Subchunk
description: Suchen nach einem Subchunk
ms.assetid: c494a57f-6395-40a4-a4f2-d200d7ad6223
keywords:
- Multimediadatei-E/A, Suchen nach DEM SEGMENT
- Datei-E/A, Suchen nach DEM SEGMENT
- Eingabe und Ausgabe (E/A), Suchen nach EINEM SEGMENT
- E/A (Eingabe und Ausgabe),Suchen nach EINEM SEGMENT
- Suchen nach DEM SEGMENT
- Resource Interchange File Format (DOSSIER)
- PROTOKOLLDATEI (Resource Interchange File Format)
- IGE E/A
- UNK-Block
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f77cc4d3b9640e0d262a113d3c8f352bb30fce625737b1bf13dde24adbe578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371138"
---
# <a name="searching-for-a-subchunk"></a>Suchen nach einem Subchunk

Im folgenden Beispiel wird die [**mmioDescend-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) verwendet, um nach dem "FMT"-Block im Abschnitt "CSV" des vorherigen Beispiels zu suchen.


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



Um nach einem Unterkunk zu suchen (d. h. nach einem beliebigen Block außer einem "CSV" oder "LIST"-Block), identifizieren Sie den übergeordneten Block im *lpckParent-Parameter* der [**mmioDescend-Funktion.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)

Wenn Sie keinen übergeordneten Block angeben, sollte sich die aktuelle Dateiposition am Anfang eines Blockes befinden, bevor Sie die **mmioDescend-Funktion** aufrufen. Wenn Sie einen übergeordneten Block angeben, kann sich die aktuelle Dateiposition an einer beliebigen Stelle in diesem Block befinden.

Wenn bei der Suche nach einem Subchunk ein Fehler auftritt, ist die aktuelle Dateiposition nicht definiert. Sie können die [**mmioSeek-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) und den **dwDataOffset-Member** der [**MMCKINFO-Struktur**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) verwenden, die den übergeordneten Block beschreiben, um bis zum Anfang des übergeordneten Blöckes zurück zu suchen, wie im folgenden Beispiel:


```C++
mmioSeek(hmmio, mmckinfoParent.dwDataOffset + 4, SEEK_SET); 
```



Da **dwDataOffset** den Offset bis zum Anfang des Datenteils des Blockes angibt, müssen Sie nach 4 Bytes nach **dwDataOffset** suchen, um die Dateiposition nach dem Formulartyp festzulegen.

 

 