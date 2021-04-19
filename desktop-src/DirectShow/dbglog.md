---
description: Das dbglog-Makro sendet eine Zeichenfolge an den debugausgabeort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. Dieses Makro wird bei Einzelhandels Builds ignoriert.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Dbglog-Makro (wxdebug. h)
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
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369677"
---
# <a name="dbglog-macro"></a>Dbglog-Makro

Das **dbglog** -Makro sendet eine Zeichenfolge an den debugausgabeort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. Dieses Makro wird bei Einzelhandels Builds ignoriert.

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

Bitweise Kombination von einem oder mehreren Nachrichten Typen.

</dd> <dt>

*Level* 
</dt> <dd>

Protokolliergrad für diese Nachricht.

</dd> <dt>

*pformat* 
</dt> <dd>

Eine Format Zeichenfolge im **printf** -Format.

</dd> <dt>

*...* 
</dt> <dd>

Zusätzliche Argumente für die Format Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Makro gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Debugprotokollierung für einen der Nachrichten Typen auf die angegebene Ebene oder höher festgelegt ist, sendet dieses Makro die formatierte Zeichenfolge an den debugausgabespeicherort.

Das Makro fügt der Ausgabe Zeichenfolge automatisch ein Zeilen Trennzeichen hinzu.

> [!Note]  
> Ein zusätzlicher Satz Klammern muss die Makro Parameter einschließen:

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wxdebug. h (Include Streams. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Debug-Ausgabefunktionen](debug-output-functions.md)
</dt> </dl>

 

 




