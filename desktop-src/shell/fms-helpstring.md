---
description: Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls Element hinzuzufügen
title: FMS_HELPSTRING-Struktur (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: c934409712ae740797eb3b5af0b55c50ff125342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994742"
---
# <a name="fms_helpstring-structure"></a>Struktur von "Help String" in f \_

Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfe Zeichenfolge für ein Menü oder Symbolleisten-Befehls Element hinzuzufügen

## <a name="syntax"></a>Syntax


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>Member

<dl> <dt>

**idcommand**
</dt> <dd>

Typ: **int**

</dd> <dd>

Der Bezeichner des Befehls Elements.

</dd> <dt>

**HMENU**
</dt> <dd>

Typ: **HMENU**

</dd> <dd>

Der Bezeichner der Menüleiste.

</dd> <dt>

**szhelp**
</dt> <dd>

Typ: **\_ \_ WCHAR \_ t \[ 128 \]**

</dd> <dd>

Die NULL-terminierte Zeichenfolge, die den Hilfetext empfängt.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> <dt>

[**"helpmenuitem" für "f" \_**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




