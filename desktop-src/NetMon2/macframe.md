---
description: Die MACFRAME-Struktur ist eine Vereinigung der gängigsten Anfangsprotokolle.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: MACFRAME union (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: dcff7294d2800e797b43b3a05bd25c35418c6fb466c95130b97be73f25040d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364708"
---
# <a name="macframe-union"></a>MACFRAME-Vereinigung

Die **MACFRAME-Struktur** ist eine Vereinigung der gängigsten Anfangsprotokolle.

## <a name="syntax"></a>Syntax


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>Member

<dl> <dt>

**MacHeader**
</dt> <dd>

Generischer Zeiger auf einen Frame.

</dd> <dt>

**Ethernet**
</dt> <dd>

Ethernet-Zeiger auf einen Frame.

</dd> <dt>

**Tokenring**
</dt> <dd>

Tokenringzeiger auf einen Frame.

</dd> <dt>

**Fddi**
</dt> <dd>

FDDI-Zeiger auf einen Frame.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird am häufigsten als Überlagerung verwendet. Um die Eigenschaften des ersten Protokolls zugänglich zu machen, umwandlungen Sie den Frame in den gleichen Typ wie das Protokoll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




