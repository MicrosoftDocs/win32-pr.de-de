---
description: Die SET-Struktur definiert einen Satz von Werten.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: SET-Struktur (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d66ba5dd3a977967d0020a00d5813c3f689142b1e58c631c99f9bd10fceba3ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074400"
---
# <a name="set-structure"></a>SET-Struktur

Die **SET-Struktur** definiert einen Satz von Werten.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a>Member

<dl> <dt>

**nEntries**
</dt> <dd>

Gesamtanzahl der Einträge in einem Satz.

</dd> <dt>

**lpByteTable**
</dt> <dd>

Zeiger auf ein Array von BYTE-Werten.

</dd> <dt>

**lpWordTable**
</dt> <dd>

Zeiger auf ein Array von WORD-Werten.

</dd> <dt>

**lpDwordTable**
</dt> <dd>

Zeiger auf ein Array von DWORD-Werten.

</dd> <dt>

**lpLargeIntTable**
</dt> <dd>

Zeiger auf ein Array von [LARGEINT-Strukturen.](largeint.md)

</dd> <dt>

**lpSystemTimeTable**
</dt> <dd>

Zeiger auf ein Array von SYSTEMTIME-Werten.

</dd> <dt>

**lpLabeledByteTable**
</dt> <dd>

Zeiger auf ein Array von [LABELED \_ BYTE-Strukturen.](labeled-byte.md) Jede **LABELED \_ BYTE-Struktur** definiert einen Wert und eine Bezeichnung. Netzwerkmonitor wird eine Bezeichnung angezeigt, wenn ein entsprechender Wert im Protokollpaket gefunden wird.

</dd> <dt>

**lpLabeledWordTable**
</dt> <dd>

Zeiger auf ein Array von [LABELED \_ WORD-Strukturen,](labeled-word.md) die einen Satz von WORD-Werten und -Bezeichnungen definieren.

</dd> <dt>

**lpLabeledDwordTable**
</dt> <dd>

Zeiger auf ein Array von [ \_ LABELED-DWORD-Strukturen,](labeled-dword.md) die einen Satz von DWORD-Werten und -Bezeichnungen definieren.

</dd> <dt>

**lpLabeledLargeIntTable**
</dt> <dd>

Zeiger auf ein Array von [LABELED \_ LARGEINT-Strukturen,](labeled-largeint.md) die einen Satz von LARGEINT-Werten und -Bezeichnungen definieren.

</dd> <dt>

**lpLabeledSystemTimeTable**
</dt> <dd>

Zeiger auf ein Array von [LABELED \_ SYSTEMTIME-Strukturen,](labeled-systemtime.md) die einen Satz von SYSTEM-Werten und -Bezeichnungen definieren.

</dd> <dt>

**lpLabeledBit**
</dt> <dd>

Zeiger auf ein Array von [LABELED \_ BIT-Strukturen,](labeled-bit.md) die einen Satz bezeichneter BIT-Paare definieren. Jedes BIT kann zwei Bezeichnungen angeben, eine Bezeichnung für jeden Zustand (0 oder 1) des BIT.

</dd> <dt>

**lpVoidTable**
</dt> <dd>

Zeiger auf ein Array von Werten.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **SET-Struktur** wird verwendet, um einen Satz von Vergleichsdaten zu definieren, Netzwerkmonitor den Wert einer Eigenschaft in einem Protokollpaket interpretieren können. Wenn ein Satz von Vergleichsdaten erforderlich ist, wird ein Zeiger auf die **SET-Struktur** im **lpSet-Member** der [PROPERTYINFO-Struktur](propertyinfo.md) angegeben.

Die Parser-DLL kann einen Wertsatz und einen Bezeichnungssatz bereitstellen. Der Member der **UNION,** den Sie in einer **SET-Struktur** auswählen, zeigt auf ein Array von Strukturen, die jeden Member einer Menge definieren.

-   Festgelegter Wert

    Ein festgelegter Wert wird verwendet, wenn Netzwerkmonitor einen festgelegten oder nicht festgelegten Indikator mit dem Im Protokollpaket gefundenen Wert enthalten soll. Wenn beispielsweise ein DWORD-Satz angegeben wird, zeigt Netzwerkmonitor eine Bezeichnung für jeden im Protokollpaket gefundenen DWORD-Wert an, der angibt, dass das DWORD im Satz angegeben ist oder nicht angegeben ist.

    Ein Wertsatz kann auf den Datentypen BYTE, WORD, DWORD, LARGEINT und SYSTEMTIME basieren.

-   Bezeichnungssatz

    Ein Bezeichnungssatz wird verwendet, wenn Netzwerkmonitor benutzerdefinierte Bezeichnung anstelle der in einem Satz angegebenen Eigenschaftswerte anzeigen soll.

    Ein Bezeichnungssatz kann auf BYTE-, WORD-, DWORD-, LARGEINT-, SYSTEMTIME- und BIT-Bezeichnungspaaren basieren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[BEZEICHNETES \_ BIT](labeled-bit.md)
</dt> <dt>

[Propertyinfo](propertyinfo.md)
</dt> </dl>

 

 




