---
description: Stellt Informationen über einen Frame in der Aufruf Liste dar.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Callstackframe-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342729"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>Callstackframe-Struktur

Stellt Informationen über einen Frame in der Aufruf Liste dar.

## <a name="syntax"></a>Syntax


```C++
} CallStackFrame;
```

## <a name="members"></a>Member

**FunctionName**  
Eine com-Zeichenfolge, die den Namen der zugeordneten Funktion enthält.

**SourceFile**  
Eine com-Zeichenfolge, die den filePath der zugeordneten Quelldatei enthält.

**ModuleName**  
Eine com-Zeichenfolge, die den Namen des zugeordneten Codemoduls enthält.

**LineNumber**  
Die zugeordnete Zeilennummer.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



