---
title: Abrufen von Informationen zu Sprech- und Dekomprimierern
description: Abrufen von Informationen zu Sprech- und Dekomprimierern
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Videokomprimierungs-Manager (Video Compression Manager, VCM), Abrufen von Informationen zu Komprimierungsdateien
- VCM (Videokomprimierungs-Manager), Abrufen von Informationen zu Komprimierung
- ICGetInfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b023a8f82fa92aa78a2a2dcf47a8f6c9447f943ac0f68440c6d7aff3123fc84e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038440"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Abrufen von Informationen zu Sprech- und Dekomprimierern

Im folgenden Beispiel wird die [**ICGetInfo-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) verwendet, um Informationen zu einem Komprimierungs- oder Dekomprimierer zu erhalten.


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



Im folgenden Beispiel werden die [**Makros ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) und [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) verwendet, um die Standardwerte zu erhalten.


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



Im folgenden Beispiel werden die [**Makros ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) und [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) verwendet, um ein Dialogfeld "About" für die Bzw. den Dekomprimierer anzuzeigen, sofern das Dialogfeld vorhanden ist.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




