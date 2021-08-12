---
description: Stellt Informationen zu einem einzelnen Eintrag im Pufferlayout eines Gitternetzes dar.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MeshDataBufferLayoutEntry-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44cc67402c69b690ba9070fa51bf8d26f316faa7d10ac991226db2c05b6d6a6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282272"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry-Struktur

Stellt Informationen zu einem einzelnen Eintrag im Pufferlayout eines Gitternetzes dar.

## <a name="syntax"></a>Syntax


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Member

**pName**  
Eine COM-Zeichenfolge, die den Namen des Eintrags enthält.

**numComponents**  
Die Anzahl homogener Komponenten (Werte), aus denen dieser Eintrag besteht.

**isPosition**  
TRUE, wenn der Eintrag eine Position ist; andernfalls FALSE.

**format**  
Das Datenformat des Eintrags (Register). Weitere Informationen finden Sie unter REGISTER \_ FORMAT-Enumeration.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



