---
description: Stellt Informationen zu einem Frame in der Aufrufstapel dar.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallStackFrame-Struktur
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
ms.openlocfilehash: c6cb4b0e32213165149d7df8c7bf334049e37399
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631338"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>CallStackFrame-Struktur

Stellt Informationen zu einem Frame in der Aufrufstapel dar.

## <a name="syntax"></a>Syntax


```C++
} CallStackFrame;
```

## <a name="members"></a>Member

**Functionname**  
Eine COM-Zeichenfolge, die den Namen der zugeordneten Funktion enthält.

**Sourcefile**  
Eine COM-Zeichenfolge, die den Dateipfad der zugeordneten Quelldatei enthält.

**moduleName**  
Eine COM-Zeichenfolge, die den Namen des zugeordneten Codemoduls enthält.

**Linenumber**  
Die zugeordnete Zeilennummer.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



