---
description: Die Set-Struktur definiert einen Satz von Werten.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: Struktur festlegen (Netmon. h)
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
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216029"
---
# <a name="set-structure"></a>Struktur festlegen

Die **Set** -Struktur definiert einen Satz von Werten.

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

**nentries**
</dt> <dd>

Die Gesamtanzahl der Einträge in einer Menge.

</dd> <dt>

**lpbytetable**
</dt> <dd>

Zeiger auf ein Array von Byte Werten.

</dd> <dt>

**lpwordtable**
</dt> <dd>

Zeiger auf ein Array von Wort Werten.

</dd> <dt>

**lpdwordtable**
</dt> <dd>

Zeiger auf ein Array von DWORD-Werten.

</dd> <dt>

**lplargeingetbar**
</dt> <dd>

Zeiger auf ein Array von [largeint](largeint.md) -Strukturen.

</dd> <dt>

**lpsystemplan**
</dt> <dd>

Zeiger auf ein Array von SYSTEMTIME-Werten.

</dd> <dt>

**lplabeledbytetable**
</dt> <dd>

Zeiger auf ein Array von [markierten \_ Byte](labeled-byte.md) Strukturen. Jede **bezeichnete \_ Byte** Struktur definiert einen Wert und eine Bezeichnung. Netzwerkmonitor eine Bezeichnung anzeigt, wenn ein entsprechender Wert im Protokoll Paket gefunden wird.

</dd> <dt>

**lplabeledwordtable**
</dt> <dd>

Ein Zeiger auf ein Array von [gekennzeichneten \_ Word](labeled-word.md) -Strukturen, die einen Satz von Wort Werten und Beschriftungen definieren.

</dd> <dt>

**lplabeleddwordtable**
</dt> <dd>

Ein Zeiger auf ein Array mit [beschrifteten \_ DWORD](labeled-dword.md) -Strukturen, die einen Satz von DWORD-Werten und-Bezeichnungen definieren.

</dd> <dt>

**lplabeledlargeintbar**
</dt> <dd>

Zeiger auf ein Array mit [beschrifteten \_ largeint](labeled-largeint.md) -Strukturen, die einen Satz von largeint-Werten und-Bezeichnungen definieren.

</dd> <dt>

**lplabeledsystemplan**
</dt> <dd>

Zeiger auf ein Array von [bezeichneten \_ SYSTEMTIME](labeled-systemtime.md) -Strukturen, die einen Satz von System Werten und Beschriftungen definieren.

</dd> <dt>

**lplabeledbit**
</dt> <dd>

Ein Zeiger auf ein Array von [beschrifteten \_ bitstrukturen](labeled-bit.md) , die einen Satz von gekennzeichneten Bitpaaren definieren. Jedes Bit kann zwei Bezeichnungen jeweils eine Bezeichnung für jeden Zustand (0 oder 1) des Bits angeben.

</dd> <dt>

**lpvoidtable**
</dt> <dd>

Zeiger auf ein Array von-Werten.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Set** -Struktur wird verwendet, um einen Satz von Vergleichsdaten zu definieren, die Netzwerkmonitor verwenden können, um den Wert einer Eigenschaft in einem Protokoll Paket zu interpretieren. Wenn ein Satz von Vergleichsdaten erforderlich ist, wird ein Zeiger auf die **festgelegte** Struktur im **lpset** -Member der [PropertyInfo](propertyinfo.md) -Struktur angegeben.

Die Parser-DLL kann einen Werte Satz und einen Bezeichnungs Satz bereitstellen. Der Member der **Union** , den Sie in einer **festgelegten** Struktur auswählen, verweist auf ein Array von-Strukturen, die jeden Member einer Menge definieren.

-   Wert festgelegt

    Ein festgelegter Wert wird verwendet, wenn Netzwerkmonitor einen in-Set-oder einen nicht in-Set-Indikator mit dem Wert enthalten soll, der im Protokoll Paket enthalten ist. Wenn z. b. ein DWORD-Satz angegeben ist, zeigt Netzwerkmonitor eine Bezeichnung für jeden DWORD-Wert an, der im Protokoll Paket enthalten ist, und gibt an, dass das DWORD-oder nicht im Satz angegeben ist.

    Ein festgelegtes Wert kann auf den Datentypen Byte, Word, DWORD, largeint und SYSTEMTIME basieren.

-   Bezeichnungs Satz

    Ein Bezeichnungs Satz wird verwendet, wenn Sie Netzwerkmonitor eine benutzerdefinierte Bezeichnung anstelle der in einer Menge angegebenen Eigenschaftswerte anzeigen möchten.

    Ein Bezeichnungs Satz kann auf Byte-, Word-, DWORD-, largeint-, SYSTEMTIME-und Bit-Bezeichnungs Paaren basieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[beschriftetes \_ Bit](labeled-bit.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> </dl>

 

 




