---
description: Die bezeichnete \_ Byte Struktur definiert ein bitpaar mit Bezeichnung. Die Bezeichnung des gekennzeichneten bitpaars wird angezeigt, wenn ein bestimmter Byte-Eigenschafts Wert erkannt wird.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: LABELED_BYTE Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357933"
---
# <a name="labeled_byte-structure"></a>Bezeichnete \_ Byte Struktur

Die **bezeichnete \_ Byte** Struktur definiert ein bitpaar mit Bezeichnung. Die **Bezeichnung des gekennzeichneten** bitpaars wird angezeigt, wenn ein bestimmter Byte-Eigenschafts Wert erkannt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a>Member

<dl> <dt>

**Wert**
</dt> <dd>

Der Bytewert der Eigenschaft, die Sie erkennen möchten.

</dd> <dt>

**Label**
</dt> <dd>

Die Textbeschreibung oder Bezeichnung, die angezeigt wird, wenn der im **Wertmember** angegebene Wert erkannt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **lplabeledbytetable** -Member der [set](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die ein **oder mehrere** Bezeichnungs Member der Byte-Wert-Paare definieren. Diese Paare werden verwendet, wenn Sie eine Bezeichnung anstelle eines bestimmten Bytewerts anzeigen möchten, der im Protokoll Paket enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

 




