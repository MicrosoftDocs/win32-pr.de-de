---
description: Stellt Informationen zum Debugsymbolserver dar.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SymbolServerInfo-Struktur
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
ms.openlocfilehash: 28f85445e6affc006c5c0898df1c85d71693a66d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632088"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo-Struktur

Stellt Informationen zum Debugsymbolserver dar.

## <a name="syntax"></a>Syntax


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Member

**symbolPath**  
Eine COM-Zeichenfolge, die den Pfad des Symbolservers enthält.

**symbolCacheDir**  
Eine COM-Zeichenfolge, die das Cacheverzeichnis des Symbolservers enthält.

**publicSymbolServerName**  
Eine COM-Zeichenfolge, die den öffentlichen Namen des Symbolservers enthält.

**symbolExcludeList**  
Eine COM-Zeichenfolge, die die Liste der auszuschließenden Symbole angibt.

**symbolIncludeList**  
Eine COM-Zeichenfolge, die die Liste der ein include-Symbole angibt.

**useExcludeList**  
TRUE, wenn die Ausschlussliste ignoriert wird; andernfalls FALSE.

**useMSSymbolServer**  
TRUE, wenn Microsoft-Symbolserver verwendet wird; andernfalls FALSE.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



