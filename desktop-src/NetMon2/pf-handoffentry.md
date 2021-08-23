---
description: Die PF \_ HANDOFFENTRY-Struktur definiert ein Protokoll, das Netzwerkmonitor dem Übergabesatz eines Parsers hinzufügt.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: PF_HANDOFFENTRY-Struktur (Netmon.h)
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
ms.openlocfilehash: faf98490424754d6ae2223ca063e0e3a4eec69c113b1a220e9657b7db5edbb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778670"
---
# <a name="pf_handoffentry-structure"></a>PF \_ HANDOFFENTRY-Struktur

Die **PF \_ HANDOFFENTRY-Struktur** definiert ein Protokoll, das Netzwerkmonitor dem Übergabesatz eines Parsers hinzufügt.

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

**szIniFile**
</dt> <dd>

Name der DEM Protokoll zugeordneten INI-Datei.

</dd> <dt>

**szIniSection**
</dt> <dd>

Abschnittsbezeichnung in der INI-Datei.

</dd> <dt>

**szProtocol**
</dt> <dd>

Der Name des Protokolls.

</dd> <dt>

**dwHandOffValue**
</dt> <dd>

Wert, der dem Protokoll zugeordnet ist.

</dd> <dt>

**ValueFormatBase**
</dt> <dd>

Numerische Basis des Protokollwerts, der in **dwHandOffValue** angegeben ist. Die **ValueFormatBase-Funktion** muss auf eine der folgenden Werte festgelegt werden:



| Wert                                                                                                                                                                                                                        | Bedeutung                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <dt>**HANDOFF \_ VALUE \_ FORMAT \_ BASE \_ UNKNOWN**</dt> </dl> | Unbekannte Basis<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <dt>**HANDOFF \_ VALUE \_ FORMAT \_ BASE \_ DECIMAL**</dt> </dl> | Dezimalbasis<br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <dt>**\_ \_ \_ \_ BASIS-HEXADEZIMALES FORMAT DES ÜBERGABEWERTFORMATS**</dt> </dl>             | Hexadezimalbasis<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Ein Array der **PF \_ HANDOFFENTRY-Strukturen** wird in der [PF \_ HANDOFFSET-Struktur](pf-handoffset.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> </dl>

 

 




