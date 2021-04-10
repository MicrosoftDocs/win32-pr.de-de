---
description: Stellt ein Histogramm einer Textur dar.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixenginehistogram-Struktur
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
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124682"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span id="vspixengine.pixenginehistogram"></span>Pixenginehistogram-Struktur

Stellt ein Histogramm einer Textur dar.

## <a name="syntax"></a>Syntax


```C++
} PixEngineHistogram;
```

## <a name="members"></a>Member

**horizontalmin**  
Die minimalen Werte für jede der X-, Y-, Z-und W-Komponenten in der horizontalen Achse (Domäne) des Histogramms.

**horizontalmax**  
Die maximalen Werte für jede der X-, Y-, Z-und W-Komponenten in der horizontalen Achse (Domäne) des Histogramms.

**verticalmin**  
Die minimalen Werte für jede der X-, Y-, Z-und W-Komponenten auf der vertikalen Achse (Bereich) des Histogramms.

**verticalmax**  
Die maximalen Werte für jede der X-, Y-, Z-und W-Komponenten auf der vertikalen Achse (Bereich) des Histogramms.

**dataLength**  
Die Anzahl der im Histogramm berücksichtigten Stichproben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



