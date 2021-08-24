---
title: Bestimmen, ob ein Treiber das Eingabeformat verarbeiten kann
description: Bestimmen, ob ein Treiber das Eingabeformat verarbeiten kann
ms.assetid: 456eab43-d830-4a28-b724-3ef35b852372
keywords:
- Videokomprimierungs-Manager (VCM), Eingabeformat
- VCM (Videokomprimierungs-Manager), Eingabeformat
- ICDrawQuery-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1453348c52ed8244ac81f830299a632f2fbe9cab03461303d9aa841dcd675666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497290"
---
# <a name="determining-if-a-driver-can-handle-the-input-format"></a>Bestimmen, ob ein Treiber das Eingabeformat verarbeiten kann

Das folgende Beispiel zeigt, wie Sie das Eingabeformat mit dem [**ICDrawQuery-Makro**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) überprüfen.


```C++
// lpbiIn points to BITMAPINFOHEADER structure indicating the input 
// format. 

if (ICDrawQuery(hIC, lpbiIn) == ICERR_OK) 
{ 
    // Driver recognizes the input format. 
} 
else 
{ 
    // Need a different decompressor. 
} 
 
```



 

 




