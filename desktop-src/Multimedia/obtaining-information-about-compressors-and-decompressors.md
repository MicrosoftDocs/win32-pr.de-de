---
title: Abrufen von Informationen zu Kompressoren und Dekompressoren
description: Abrufen von Informationen zu Kompressoren und Dekompressoren
ms.assetid: 2f1edfd0-dd30-42ea-a5ae-24265d3f8af3
keywords:
- Videokomprimierungs-Manager (VCM), Informationen zu Kompressoren erhalten
- VCM (Videokomprimierungs-Manager), Informationen zu Kompressoren erhalten
- Icgetinfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 874793233ef0aec4de5b372573fb8dcd79f5d875
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388090"
---
# <a name="obtaining-information-about-compressors-and-decompressors"></a>Abrufen von Informationen zu Kompressoren und Dekompressoren

Im folgenden Beispiel wird die [**icgetinfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) -Funktion verwendet, um Informationen zu einem Kompressor oder Dekompressor abzurufen.


```C++
ICINFO ICInfo; 
ICGetInfo(hIC, &ICInfo, sizeof(ICInfo)); 
 
```



Im folgenden Beispiel werden die Standardwerte mit den Makros [**icgetdefaultkeyframerate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) und [**icgetdefaultquality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) abgerufen.


```C++
DWORD dwKeyFrameRate, dwQuality; 
dwKeyFrameRate = ICGetDefaultKeyFrameRate(hIC); 
dwQuality = ICGetDefaultQuality(hIC); 
 
```



Im folgenden Beispiel werden die Makros [**icqueryabout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) und [**icabout**](/windows/desktop/api/Vfw/nf-vfw-icabout) verwendet, um ein Info Dialogfeld für den-Kompressor oder den-Debug anzuzeigen, wenn das Dialogfeld vorhanden ist.


```C++
// If the compressor has an About dialog box, display it.

if ( ICQueryAbout(hIC)) ICAbout(hIC, hwndApp); 
 
```



 

 




