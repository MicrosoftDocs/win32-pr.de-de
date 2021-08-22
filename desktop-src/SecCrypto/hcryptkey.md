---
description: Der HCRYPTKEY-Datentyp wird verwendet, um Handles für kryptografische Schlüssel darzustellen.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78d50f7fb005d877f6520172631b4546b8d498c415de58502defd26831c65fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006438"
---
# <a name="hcryptkey"></a>HCRYPTKEY

Der **HCRYPTKEY-Datentyp** wird verwendet, um Handles für [*kryptografische Schlüssel*](../secgloss/c-gly.md)darzustellen. Diese Handles werden verwendet, um dem CSP-Modul anzugeben, welcher Schlüssel in einem bestimmten Vorgang verwendet wird. Das CSP-Modul ermöglicht keinen direkten Zugriff auf die Schlüsselwerte. Stattdessen führt der Benutzer Funktionen aus, indem er den Schlüsselwert über das Schlüsselhandle verwendet.


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



 

 
