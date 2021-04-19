---
description: Die PF- \_ handoffentry-Struktur definiert ein Protokoll, das Netzwerkmonitor dem Übergabe Satz eines Parsers hinzufügt.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: PF_HANDOFFENTRY Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364068"
---
# <a name="pf_handoffentry-structure"></a>PF- \_ handoffentry-Struktur

Die **PF- \_ handoffentry** -Struktur definiert ein Protokoll, das Netzwerkmonitor dem Übergabe Satz eines Parsers hinzufügt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**szinifile**
</dt> <dd>

Der Name der INI-Datei, die dem Protokoll zugeordnet ist.

</dd> <dt>

**szinisection**
</dt> <dd>

Abschnitts Bezeichnung in der INI-Datei.

</dd> <dt>

**szprotocol**
</dt> <dd>

Der Name des Protokolls.

</dd> <dt>

**dwhandoffvalue**
</dt> <dd>

Der Wert, der dem Protokoll zugeordnet ist.

</dd> <dt>

**Valueformatbase**
</dt> <dd>

Numerische Basis des Protokoll Werts, der in **dwhandoffvalue** angegeben wird. Die **valueformatbase** -Funktion muss auf einen der folgenden Werte festgelegt werden:



| Wert                                                                                                                                                                                                                        | Bedeutung                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**das Format des Handoff- \_ Werts ist \_ \_ \_ unbekannt.**</dt> </dl> | Unbekannte Basis<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**Grund für das Format des Handoff- \_ Werts \_ \_ \_**</dt> </dl> | Dezimaltrennzeichen<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**Format für Übergabe \_ Wert \_ Format \_ Basis \_ Hex**</dt> </dl>             | Hexadezimale Basis<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein Array der **PF- \_ handoffentry** -Strukturen wird in der [PF- \_ handoffset](pf-handoffset.md) -Struktur verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF- \_ handoffset](pf-handoffset.md)
</dt> </dl>

 

 




