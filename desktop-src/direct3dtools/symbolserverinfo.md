---
description: Stellt Informationen zum debugsymbolserver dar.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Symbolserverinfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124154"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Symbolserverinfo-Struktur

Stellt Informationen zum debugsymbolserver dar.

## <a name="syntax"></a>Syntax


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Member

**symbolPath**  
Eine com-Zeichenfolge, die den Pfad des Symbol Servers enthält.

**symbolcachedir**  
Eine com-Zeichenfolge, die das Cache Verzeichnis des Symbol Servers enthält.

**publicsymbolservername**  
Eine com-Zeichenfolge, die den öffentlichen Namen des Symbol Servers enthält.

**symbolexcludelta ist**  
Eine com-Zeichenfolge, die die Liste der auszuschließenden Symbole angibt.

**symbolincludelta ist**  
Eine com-Zeichenfolge, die die Liste der einzuschließenden Symbole angibt.

**useexcludelta ist**  
true, wenn die Ausschlussliste ignoriert wird. andernfalls false.

**usemssymbolserver**  
true bei Verwendung von Microsoft Symbol Server; andernfalls false.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



