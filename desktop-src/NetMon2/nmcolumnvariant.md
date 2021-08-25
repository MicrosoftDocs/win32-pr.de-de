---
description: Stellt eine Zeile im oberen Bereich des Ereignisanzeige bereit, die als Container für alle möglichen Daten dient, die in eine Spalte eingefügt werden.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: NMCOLUMNVARIANT-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 814b419909591e45c07b3ed499072ec4871cdeb1f4c5a355277a03d0623d264c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890021"
---
# <a name="nmcolumnvariant-structure"></a>NMCOLUMNVARIANT-Struktur

Die **NMCOLUMNVARIANT-Struktur** stellt eine Zeile im oberen Bereich des Ereignisanzeige bereit, die als Container für alle möglichen Daten dient, die in eine Spalte eingefügt werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a>Member

<dl> <dt>

**Typ**
</dt> <dd>

Ein Wert aus dem [**NMCOLUMNTYPE-Enumerationstyp.**](nmcolumntype.md)

</dd> <dt>

**Wert**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

8-Bit-Ganzzahlwert ohne Vorzeichen.

</dd> <dt>

**Sint8Val**
</dt> <dd>

8-Bit-Ganzzahlwert mit Vorzeichen.

</dd> <dt>

**Uint16Val**
</dt> <dd>

16-Bit-Ganzzahlwert ohne Vorzeichen.

</dd> <dt>

**Sint16Val**
</dt> <dd>

16-Bit-Ganzzahlwert mit Vorzeichen.

</dd> <dt>

**Uint32Val**
</dt> <dd>

32-Bit-Ganzzahlwert ohne Vorzeichen.

</dd> <dt>

**Sint32Val**
</dt> <dd>

32-Bit-Ganzzahlwert mit Vorzeichen.

</dd> <dt>

**Float64Val**
</dt> <dd>

64-Bit-Gleitkommawert.

</dd> <dt>

**FrameVal**
</dt> <dd>

Framenummer.

</dd> <dt>

**YesNoVal**
</dt> <dd>

Zeigt Ja oder Nein an.

</dd> <dt>

**OnOffVal**
</dt> <dd>

Zeigt Ein oder Aus an.

</dd> <dt>

**TrueFalseVal**
</dt> <dd>

Zeigt True oder False an.

</dd> <dt>

**MACAddrVal**
</dt> <dd>

MAC-Adresse

</dd> <dt>

**IPXAddrVal**
</dt> <dd>

IPX-Adresse.

</dd> <dt>

**IPAddrVal**
</dt> <dd>

IP-Adresse.

</dd> <dt>

**VarTimeVal**
</dt> <dd>

Variant-Zeit. Verwenden Sie **VariantTimetoSystemTime,** um die Systemzeit zu konvertieren.

</dd> <dt>

**pStringVal**
</dt> <dd>

Zeiger auf eine Zeichenfolge.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**NMCOLUMNTYPE**](nmcolumntype.md)
</dt> </dl>

 

 




