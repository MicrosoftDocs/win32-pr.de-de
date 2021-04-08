---
description: Die patternmatch-Struktur definiert Musterelemente, die zum Auswerten eines Frames verwendet werden.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: Patternmatch-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960022"
---
# <a name="patternmatch-structure"></a>Patternmatch-Struktur

Die **patternmatch** -Struktur definiert Musterelemente, die zum Auswerten eines Frames verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a>Member

<dl> <dt>

**Flags**
</dt> <dd>

Muster Übereinstimmungs Flags:



| Wert                                                                                                                                                                                                                                                                                           | Bedeutung                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <dt>**Muster \_ Übereinstimmungs \_ Flags \_ nicht**</dt> <dt>0x00000001</dt> </dl>                                   | Wenn festgelegt, behält dieses Flag Frames bei, die das angegebene Muster nicht an der richtigen Stelle haben.<br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <dt>**Muster \_ Port der Übereinstimmungs \_ Flags \_ \_ angegeben**</dt> <dt>0x00000008</dt> </dl> | Sucht einen Wert für die Portnummer.<br/>                                                             |



 

</dd> <dt>

**Offsetbasis**
</dt> <dd>

Typen von Offset, bei denen es sich um einen der folgenden Typen handeln kann:



| Wert                                                                                                                                                                                                                                                       | Bedeutung                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <dt>**Offset- \_ Basis \_ relativ \_ zum \_ Frame**</dt> </dl>                                         | Legt einen Offset (in Bytes) relativ zum Start des Frames fest.<br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <dt>**Offset \_ - \_ Basis \_ in Bezug auf das \_ effektive \_ Protokoll**</dt> </dl> | Legt einen Offset (in Bytes) relativ zum Anfang des Protokolls fest, auf das verwiesen wird.<br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <dt>**Offset \_ - \_ Basis \_ in Bezug auf \_ IPX**</dt> </dl>                                               | Legt einen Offset (in Bytes) nur relativ zu IPX fest.<br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <dt>**Offset \_ \_ -Basis relativ \_ zu \_ IP**</dt> </dl>                                                  | Legt einen Offset (in Bytes) nur relativ zu IP fest.<br/>                              |



 

</dd> <dt>

**Port**
</dt> <dd>

Der Portwert, falls angegeben.

</dd> <dt>

**Offset**
</dt> <dd>

Der Offset in Bytes relativ zu **Offsetbasis**.

</dd> <dt>

**Länge**
</dt> <dd>

Länge des übereinstimmenden Musters.

</dd> <dt>

**Patterntomatch**
</dt> <dd>

Das zu Übereinstimmungs Muster.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird verwendet, um einen Erfassungs Filter zu erstellen. Weitere Informationen zum Implementieren dieser Struktur finden Sie unter [Erfassungs Filter](capture-filters.md).

Ein Erfassungs Filter kann bis zu vier **patternmatch** -Strukturen enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Capturefilter](capturefilter.md)
</dt> </dl>

 

 




