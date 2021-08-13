---
description: Stellt ein Histogramm einer Textur dar.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixEngineHistogram-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: afa9de8ecb598c76daee56367cc9f3ee80a0d0a43f706d11d2eaaa33cd814f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282309"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram-Struktur

Stellt ein Histogramm einer Textur dar.

## <a name="syntax"></a>Syntax


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Member

**horizontalMin**  
Die Mindestwerte für jede X-, Y-, Z- und W-Komponente auf der horizontalen Achse (Domäne) des Histogramms.

**horizontalMax**  
Die Maximalenwerte für jede der X-, Y-, Z- und W-Komponenten auf der horizontalen Achse (Domäne) des Histogramms.

**verticalMin**  
Die Mindestwerte für jede der X-, Y-, Z- und W-Komponenten in der vertikalen Achse (Bereich) des Histogramms.

**verticalMax**  
Die maximalen Werte für die einzelnen X-, Y-, Z- und W-Komponenten in der vertikalen Achse (Bereich) des Histogramms.

**Datalength**  
Die Anzahl der im Histogramm berücksichtigten Stichproben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



