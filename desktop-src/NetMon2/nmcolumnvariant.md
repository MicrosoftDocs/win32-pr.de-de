---
description: Stellt eine Linie im oberen Bereich der Ereignisanzeige bereit, die als Container für alle möglichen Daten dient, die in eine Spalte eingefügt werden.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Nmcolumnvariant-Struktur (Netmon. h)
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
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352765"
---
# <a name="nmcolumnvariant-structure"></a>Nmcolumnvariant-Struktur

Die **nmcolumnvariant** -Struktur stellt eine Linie im oberen Bereich der Ereignisanzeige bereit, die als Container für alle möglichen Daten dient, die in eine Spalte eingefügt werden.

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

**Type**
</dt> <dd>

Ein Wert aus dem [**nmcolumntype**](nmcolumntype.md) -Enumerationstyp.

</dd> <dt>

**Wert**
</dt> <dd> <dl> <dt>

**Uint8Val**
</dt> <dd>

ganzzahliger 8-Bit-Wert ohne Vorzeichen.

</dd> <dt>

**Sint8Val**
</dt> <dd>

ganzzahliger 8-Bit-Wert mit Vorzeichen.

</dd> <dt>

**Uint16Val**
</dt> <dd>

ganzzahliger 16-Bit-Wert ohne Vorzeichen.

</dd> <dt>

**Sint16Val**
</dt> <dd>

ganzzahliger 16-Bit-Wert mit Vorzeichen.

</dd> <dt>

**Uint32Val**
</dt> <dd>

32-Bit-Ganzzahl ohne Vorzeichen.

</dd> <dt>

**Sint32Val**
</dt> <dd>

32-Bit-Ganzzahl mit Vorzeichen.

</dd> <dt>

**Float64Val**
</dt> <dd>

64-Bit-Float-Wert.

</dd> <dt>

**Frameval**
</dt> <dd>

Frame Nummer.

</dd> <dt>

**Yesnoval**
</dt> <dd>

Zeigt ja oder Nein an.

</dd> <dt>

**Onoffval**
</dt> <dd>

Wird ein-oder ausgeschaltet angezeigt.

</dd> <dt>

**Truefalsee Val**
</dt> <dd>

Zeigt True oder false an.

</dd> <dt>

**Macaddrval**
</dt> <dd>

MAC-Adresse

</dd> <dt>

**Ipxaddrval**
</dt> <dd>

IPX-Adresse

</dd> <dt>

**Ipaddrval**
</dt> <dd>

IP-Adresse.

</dd> <dt>

**Vartimeval**
</dt> <dd>

Variant-Zeit. Verwenden Sie **varianttimeumsystemtime** , um in die Systemzeit zu konvertieren.

</dd> <dt>

**pstringval**
</dt> <dd>

Zeiger auf eine Zeichenfolge.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Nmcolumntype**](nmcolumntype.md)
</dt> </dl>

 

 




