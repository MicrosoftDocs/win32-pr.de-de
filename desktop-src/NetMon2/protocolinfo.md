---
description: Die protocolinfo-Struktur beschreibt ein Protokoll.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Protocolinfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373193"
---
# <a name="protocolinfo-structure"></a>Protocolinfo-Struktur

Die **protocolinfo** -Struktur beschreibt ein Protokoll.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Protokolid**
</dt> <dd>

Die vom System zugewiesene Protokoll Kennung der angegebenen Lauf Sitzung.

</dd> <dt>

**Propertydatabase**
</dt> <dd>

Die Eigenschaften Datenbank des angegebenen Protokolls.

</dd> <dt>

**ProtocolName**
</dt> <dd>

Abgekürzte Protokoll Name.

</dd> <dt>

**HelpFile**
</dt> <dd>

Optionaler Name der Hilfedatei, die dem Protokoll zugeordnet ist.

</dd> <dt>

**Kommentar**
</dt> <dd>

Ein Kommentar, der das Protokoll beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




