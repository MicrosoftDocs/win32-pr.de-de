---
description: Die macframe-Struktur ist eine Vereinigung der gängigsten anfänglichen Protokolle.
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: Macframe-Union (Netmon. h)
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
ms.openlocfilehash: a7901daf467a63586543c52ca8a214d5d0094982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357368"
---
# <a name="macframe-union"></a>Macframe-Union

Die **macframe** -Struktur ist eine Vereinigung der gängigsten anfänglichen Protokolle.

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

**Machereader**
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

**FDDI**
</dt> <dd>

FDDI-Zeiger auf einen Frame.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird am häufigsten als Überlagerung verwendet. Um die Eigenschaften des ersten Protokolls zugänglich zu machen, wandeln Sie den Frame in denselben Typ wie das Protokoll um.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




