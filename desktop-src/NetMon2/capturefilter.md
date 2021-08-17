---
description: Die CAPTUREFILTER-Struktur enthält Erfassungsfilterdaten.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: CAPTUREFILTER-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILTER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: de5ab95ab395d50afb41223a458342706da1df7434d524f21c230436b3b9c7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796360"
---
# <a name="capturefilter-structure"></a>CAPTUREFILTER-Struktur

Die **CAPTUREFILTER-Struktur** enthält Erfassungsfilterdaten.

## <a name="syntax"></a>Syntax


```C++
typedef struct _CAPTUREFILTER {
  DWORD          FilterFlags;
  LPBYTE         lpSapTable;
  LPWORD         lpEtypeTable;
  WORD           nSaps;
  WORD           nEtypes;
  LPADDRESSTABLE AddressTable;
  EXPRESSION     FilterExpression;
  TRIGGER        Trigger;
  DWORD          nFrameBytesToCopy;
  RESERVED       Reserved;
} CAPTUREFILTER, *LPCAPTUREFILTER;
```



## <a name="members"></a>Member

<dl> <dt>

**FilterFlags**
</dt> <dd>

Flags, die den Inhalt des Erfassungsfilters beschreiben.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**CAPTUREFILTER \_ FLAGS \_ UMFASSEN \_ ALLE \_ SAPS-0x0001**</dt> <dt></dt> </dl>       | Schließt alle SAPs als akzeptable Frames ein.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**CAPTUREFILTER \_ FLAGS \_ INCLUDE \_ ALL \_ ETYPES**</dt> <dt>0x0002</dt> </dl> | Schließen Sie alle E-Datentypen als akzeptable Frames ein.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**CAPTUREFILTER \_ FLAGS \_ \_ LOCAL ONLY**</dt> <dt>0x0008</dt> </dl>                          | Kein P-Modus<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**CAPTUREFILTER \_ FLAGS \_ KEEP \_ RAW**</dt> <dt>0x0020</dt> </dl>                                | Behalten Sie SMT- und Tokenring-MAC-Frames bei.<br/>      |



 

</dd> <dt>

**lpSapTable**
</dt> <dd>

Zeiger auf ein Array von SAP-Werten. Dieser Member gibt die SAP-Werte an, die an den Treiber übergeben werden dürfen. Wenn CAPTUREFILTER \_ FLAGS \_ INCLUDE ALL \_ \_ SAPS festgelegt ist, wird dies zu einer Ausnahmeliste (einschließlich aller SAPS außer diesen).

</dd> <dt>

**lpEtypeTable**
</dt> <dd>

Zeiger auf ein Array von Etype-Werten. Dies gibt die Etype-Werte an, die an den Treiber übergeben werden dürfen. Wenn CAPTUREFILTER \_ FLAGS \_ INCLUDE ALL \_ \_ ETYPES festgelegt ist, wird dies zu einer Ausnahmeliste (alle Etypes mit Ausnahme dieser einschließen).

</dd> <dt>

**nSaps**
</dt> <dd>

Anzahl der SAPs in der SAP-Tabelle.

</dd> <dt>

**nEtypes**
</dt> <dd>

Anzahl der Etypes in der Etype-Tabelle.

</dd> <dt>

**AddressTable**
</dt> <dd>

Name der Adresstabelle.

</dd> <dt>

**Filterexpression**
</dt> <dd>

Eine EXPRESSION-Struktur. Dies enthält den Muster match-Teil des Erfassungsfilters.

</dd> <dt>

**Trigger**
</dt> <dd>

Reserviert.

</dd> <dt>

**nFrameBytesToCopy**
</dt> <dd>

Wenn dieser Member nicht 0 ist, gibt er an, wie viele Bytes für jeden empfangenen Frame beibehalten werden sollen. Wenn es 0 ist, behalten Sie den gesamten Frame bei.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Kombination aus Flags, Werten und Ausdrücken bestimmt, welche Frames vom Treiber übergeben werden, der diese Strukturdaten verwendet. Weitere Informationen zum Implementieren einer **CAPTUREFILTER-Struktur** finden Sie unter [Capture Filters](capture-filters.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ADDRESSTABLE](addresstable.md)
</dt> <dt>

[ADDRESSPAIR](addresspair.md)
</dt> <dt>

[Ausdruck](expression.md)
</dt> <dt>

[ANDEXP](andexp.md)
</dt> <dt>

[PATTERNMATCH](patternmatch.md)
</dt> </dl>

 

 




