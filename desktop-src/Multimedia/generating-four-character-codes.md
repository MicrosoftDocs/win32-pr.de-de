---
title: Generieren von Four-Character Codes
description: Generieren von Four-Character Codes
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- Multimediadatei-E/A, vierstellige Codes
- Datei-E/A, Vier-Zeichen-Codes
- Eingabe und Ausgabe (E/A), vierstellige Codes
- E/A (Eingabe und Ausgabe), Vier-Zeichen-Codes
- Vierstellige Codes
- mmioStringToFOURCC-Funktion
- mmioFOURCC-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96dd724876a3c4b6ac37424b49411edac5929c61d1fcf6c8c18275b1d6ae9dd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785310"
---
# <a name="generating-four-character-codes"></a>Generieren von Four-Character Codes

Sie können das [**MmioFOURCC-Makro**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) oder die [**mmioStringToFOURCC-Funktion**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) verwenden, um Vier-Zeichen-Codes zu generieren. Im folgenden Beispiel wird **mmioFOURCC** verwendet, um einen vierstelligen Code für "WAVE" zu generieren.


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



Im folgenden Beispiel wird [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) verwendet, um einen vierstelligen Code für "WAVE" zu generieren.


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



Der zweite Parameter in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) gibt Flags zum Konvertieren der Zeichenfolge in einen vierstelligen Code an. Wenn Sie das MMIO \_ TOUPPER-Flag angeben, konvertiert **mmioStringToFOURCC** alle alphabetischen Zeichen in der Zeichenfolge in Großbuchstaben. Dies ist nützlich, wenn Sie einen vierstelligen Code angeben müssen, um eine benutzerdefinierte E/A-Prozedur zu identifizieren, da vierstellige Codes, die Dateierweiterungsnamen identifizieren, groß geschrieben werden müssen.

 

 