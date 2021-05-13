---
description: Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement hinzuzufügen.
title: FMS_HELPSTRING-Struktur (Wfext.h)
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
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842211"
---
# <a name="fms_helpstring-structure"></a>FMS \_ HELPSTRING-Struktur

Enthält Informationen, die der Datei-Manager verwendet, um eine Hilfezeichenfolge für ein Menü- oder Symbolleistenbefehlselement hinzuzufügen.

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

**idCommand**
</dt> <dd>

Typ: **INT**

</dd> <dd>

Der Bezeichner des Befehlselements.

</dd> <dt>

**Hmenu**
</dt> <dd>

Typ: **HMENU**

</dd> <dd>

Der Bezeichner der Menüleiste.

</dd> <dt>

**szHelp**
</dt> <dd>

Typ: **\_ \_ wchar \_ t \[ 128 \]**

</dd> <dd>

Die auf NULL endende Zeichenfolge, die den Hilfetext empfängt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




