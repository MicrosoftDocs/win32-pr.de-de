---
description: Die dbgsetmodulelevel-Funktion legt den Protokolliergrad für einen oder mehrere Nachrichten Typen fest. Wird in Einzelhandels Builds ignoriert.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: Dbgsetmodulelevel-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358381"
---
# <a name="dbgsetmodulelevel-function"></a>Dbgsetmodulelevel-Funktion

Die **dbgsetmodulelevel** -Funktion legt den Protokolliergrad für einen oder mehrere Nachrichten Typen fest. Wird in Einzelhandels Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgSetModuleLevel(
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

Protokolliergrad für die angegebenen Nachrichten Typen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




