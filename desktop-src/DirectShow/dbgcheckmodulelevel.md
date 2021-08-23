---
description: Die DbgCheckModuleLevel-Funktion überprüft, ob die Protokollierung für die angegebenen Nachrichtentypen und -ebenen aktiviert ist. Wird in Einzelhandels-Builds ignoriert.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: DbgCheckModuleLevel-Funktion (Wxdebug.h)
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
ms.openlocfilehash: dd6d7c61e7989987401c22386054c02f87410ce66dbb98bb6e20a813f2c851be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823700"
---
# <a name="dbgcheckmodulelevel-function"></a>DbgCheckModuleLevel-Funktion

Die `DbgCheckModuleLevel` Funktion überprüft, ob die Protokollierung für die angegebenen Nachrichtentypen und -ebene aktiviert ist. Wird in Einzelhandels-Builds ignoriert.

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

Bitweise Kombination eines oder mehrerer Nachrichtentypen.

</dd> <dt>

*Level* 
</dt> <dd>

Protokolliergrad

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die Protokollierung für einen der angegebenen Nachrichtentypen auf die angegebene Ebene oder höher festgelegt ist. Andernfalls wird **FALSE zurückgegeben.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Debugausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




