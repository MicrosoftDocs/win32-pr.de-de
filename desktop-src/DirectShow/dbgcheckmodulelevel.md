---
description: Die dbgcheckmodulelevel-Funktion überprüft, ob die Protokollierung für die angegebenen Nachrichten Typen und die angegebene Ebene aktiviert ist. Wird in Einzelhandels Builds ignoriert.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: Dbgcheckmodulelevel-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373978"
---
# <a name="dbgcheckmodulelevel-function"></a>Dbgcheckmodulelevel-Funktion

Die `DbgCheckModuleLevel` -Funktion überprüft, ob die Protokollierung für die angegebenen Nachrichten Typen und-Ebenen aktiviert ist. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typen* 
</dt> <dd>

Bitweise Kombination von einem oder mehreren Nachrichten Typen.

</dd> <dt>

*Level* 
</dt> <dd>

Protokolliergrad

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Protokollierung für einen der angegebenen Nachrichten Typen auf die angegebene Ebene oder höher festgelegt ist. Andernfalls wird **false** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




