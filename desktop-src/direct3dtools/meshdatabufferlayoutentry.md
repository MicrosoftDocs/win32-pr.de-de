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
ms.openlocfilehash: 40360e73f480b4c12dcb24311c26fd9718093705
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625356"
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

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



