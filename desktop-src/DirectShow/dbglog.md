---
description: Das DbgLog-Makro sendet eine Zeichenfolge an den Debugausgabespeicherort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. Dieses Makro wird in Einzelhandels-Builds ignoriert.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: DbgLog-Makro (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 619a3cd277425b555bc64139c3e59c959cc6abd19d6da22c2129830c38496a24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953339"
---
# <a name="dbglog-macro"></a>DbgLog-Makro

Das **DbgLog-Makro** sendet eine Zeichenfolge an den Debugausgabespeicherort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. Dieses Makro wird in Einzelhandels-Builds ignoriert.

## <a name="syntax"></a>Syntax


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
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

Protokollierstufe für diese Meldung.

</dd> <dt>

*pFormat* 
</dt> <dd>

Eine **Formatzeichenfolge im Printf-Format.**

</dd> <dt>

*...* 
</dt> <dd>

Zusätzliche Argumente für die Formatzeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die Debugprotokollierung für einen der Nachrichtentypen auf die angegebene Ebene oder höher festgelegt ist, sendet dieses Makro die formatierte Zeichenfolge an den Debugausgabespeicherort.

Das Makro fügt der Ausgabezeichenfolge automatisch ein Neue-Zeichen hinzu.

> [!Note]  
> Ein zusätzlicher Satz von Klammern muss die Makroparameter umschließen:

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug.h (include Streams.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Debugausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




