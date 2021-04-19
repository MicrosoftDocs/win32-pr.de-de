---
description: Die capturefilter-Struktur enthält Erfassungs Filterdaten.
ms.assetid: 773187c6-31c7-4439-850d-1dd43d42f701
title: Capturefilter-Struktur (Netmon. h)
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
ms.openlocfilehash: 129575ba401aed0e78f52695a49139f4143c9c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358563"
---
# <a name="capturefilter-structure"></a>Capturefilter-Struktur

Die **capturefilter** -Struktur enthält Erfassungs Filterdaten.

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

**Filterflags**
</dt> <dd>

Flags, die den Inhalt des Erfassungs Filters beschreiben.



| Wert                                                                                                                                                                                                                                                                                                   | Bedeutung                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_SAPS"></span><span id="capturefilter_flags_include_all_saps"></span><dl> <dt>**Capturefilter \_ Flags \_ enthalten \_ alle \_ SAPS**</dt> <dt>0x0001</dt> </dl>       | Schließt alle SAPS als akzeptable Frames ein.<br/>  |
| <span id="CAPTUREFILTER_FLAGS_INCLUDE_ALL_ETYPES"></span><span id="capturefilter_flags_include_all_etypes"></span><dl> <dt>**Capturefilter \_ Flags \_ enthalten \_ alle \_ ETYPEs**</dt> <dt>0x0002</dt> </dl> | Alle ETYPEs als akzeptable Frames einschließen.<br/> |
| <span id="CAPTUREFILTER_FLAGS_LOCAL_ONLY"></span><span id="capturefilter_flags_local_only"></span><dl> <dt>**Capturefilter \_ Flags \_ \_ nur lokal**</dt> <dt>0x0008</dt> </dl>                          | Kein P-Modus<br/>                                |
| <span id="CAPTUREFILTER_FLAGS_KEEP_RAW"></span><span id="capturefilter_flags_keep_raw"></span><dl> <dt>**Capturefilter \_ Flags \_ behalten den \_ Rohdaten**</dt> - <dt>0x0020</dt> bei </dl>                                | Halten Sie SMT-und TokenRing-Mac-Frames<br/>      |



 

</dd> <dt>

**lpsaptable**
</dt> <dd>

Zeiger auf ein Array von SAP-Werten. Dieser Member gibt die SAP-Werte an, die für die Übergabe an den Treiber gültig sind. Wenn die capturefilter- \_ Flags \_ \_ alle \_ SAPS enthalten, wird dies zu einer Ausnahmeliste (einschließlich aller SAPS außer diesen).

</dd> <dt>

**lpeer typetable**
</dt> <dd>

Zeiger auf ein Array von ETYPE-Werten. Dies gibt die ETYPE-Werte an, die für die Übergabe an den Treiber gültig sind. Wenn die capturefilter- \_ Flags \_ \_ alle \_ ETYPEs festgelegt sind, wird dies zu einer Ausnahmeliste (alle ETYPEs mit Ausnahme dieser).

</dd> <dt>

**NSAPs**
</dt> <dd>

Anzahl der SAPS in der SAP-Tabelle.

</dd> <dt>

**"ntypes"**
</dt> <dd>

Anzahl der ETYPEs in der ETYPE-Tabelle.

</dd> <dt>

**Adresssstable**
</dt> <dd>

Der Name der Adress Tabelle.

</dd> <dt>

**Filter Expression**
</dt> <dd>

Eine Ausdrucks Struktur. Diese enthält den Muster Übereinstimmungs Teil des Erfassungs Filters.

</dd> <dt>

**Trigger**
</dt> <dd>

Reserviert.

</dd> <dt>

**nframebytestokopie**
</dt> <dd>

Wenn dieser Member nicht 0 ist, gibt er an, wie viele Bytes für jeden empfangenen Frame aufbewahrt werden. Wenn der Wert 0 ist, behalten Sie den gesamten Frame bei.

</dd> <dt>

**Reserved**
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Kombination aus Flags, Werten und Ausdrücken bestimmt, welche Frames vom Treiber, der diese Strukturdaten verwendet, übermittelt werden. Weitere Informationen zum Implementieren einer **capturefilter** -Struktur finden Sie unter [Capture Filters](capture-filters.md)(Aufzeichnen von Filtern).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Adresssstable](addresstable.md)
</dt> <dt>

[Adresssspair](addresspair.md)
</dt> <dt>

[Begriff](expression.md)
</dt> <dt>

[Andexp](andexp.md)
</dt> <dt>

[Patternmatch](patternmatch.md)
</dt> </dl>

 

 




