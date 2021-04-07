---
title: Erstellen von Four-Character Codes
description: Erstellen von Four-Character Codes
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- Multimedia-Datei-e/a, vier Zeichen Codes
- Datei-e/a, vier Zeichen Codes
- Eingabe und Ausgabe (e/a), vier Zeichen Codes
- E/a (Eingabe und Ausgabe), vier Zeichen Codes
- vier Zeichen Codes
- mmiostringto FourCC-Funktion
- mmiofourcc-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725121"
---
# <a name="generating-four-character-codes"></a>Erstellen von Four-Character Codes

Sie können das [**mmiofourcc**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) -Makro oder die [**mmiostringesfourcc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) -Funktion verwenden, um vier Zeichen Codes zu generieren. Im folgenden Beispiel wird **mmiofourcc** verwendet, um einen vierstelligen Code für "Wave" zu generieren.


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



Im folgenden Beispiel wird [**mmiostringdefourcc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) verwendet, um einen vierstelligen Code für "Wave" zu generieren.


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



Mit dem zweiten Parameter in [**mmiostringumfourcc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) werden Flags zum umrechnen der Zeichenfolge in einen aus vier Zeichen bestehende Code angegeben. Wenn Sie das MMIO- \_ toupperflag angeben, konvertiert **mmiostringumfourcc** alle alphabetischen Zeichen in der Zeichenfolge in Großbuchstaben. Dies ist hilfreich, wenn Sie einen aus vier Zeichen bestehende Code angeben müssen, um eine benutzerdefinierte e/a-Prozedur zu identifizieren, da vier Zeichen Codes, die Datei Erweiterungs Namen identifizieren, Großbuchstaben sein müssen.

 

 