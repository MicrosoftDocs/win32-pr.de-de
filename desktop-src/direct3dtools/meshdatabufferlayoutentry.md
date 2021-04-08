---
description: Stellt Informationen zu einem einzelnen Eintrag im Puffer Layout eines Netzes dar.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Meshdatabufferlayoutentry-Struktur
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
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747576"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span id="vspixengine.meshdatabufferlayoutentry"></span>Meshdatabufferlayoutentry-Struktur

Stellt Informationen zu einem einzelnen Eintrag im Puffer Layout eines Netzes dar.

## <a name="syntax"></a>Syntax


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a>Member

**pName**  
Eine com-Zeichenfolge, die den Namen des Eintrags enthält.

**numcomponents**  
Die Anzahl der homogenen Komponenten (Werte), aus denen dieser Eintrag besteht.

**isposition**  
true, wenn der Eintrag eine Position ist. andernfalls false.

**format**  
Das Datenformat des Eintrags (Register). Weitere Informationen finden Sie unter Register \_ Format-Enumeration.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



