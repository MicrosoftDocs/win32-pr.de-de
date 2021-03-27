---
description: Enthält Informationen über eine Schaltfläche, die von einer Datei-Manager-Erweiterungs-DLL der Symbolleiste des Datei-Managers hinzugefügt wird.
title: EXT_BUTTON-Struktur (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751016"
---
# <a name="ext_button-structure"></a>Struktur der Ext- \_ Taste

Enthält Informationen über eine Schaltfläche, die von einer Datei-Manager-Erweiterungs-DLL der Symbolleiste des Datei-Managers hinzugefügt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>Member

<dl> <dt>

**idcommand**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Ein Befehls Bezeichner für die Schaltfläche.

</dd> <dt>

**idshelp**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Bezeichner der Hilfe Zeichenfolge für die Schaltfläche.

</dd> <dt>

**fsstyle**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Stil der Schaltfläche.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"Tool barload" von "f" \_**](fmevent-toolbarload.md)
</dt> <dt>

[**f- \_ Toolbar laden**](fms-toolbarload.md)
</dt> </dl>

 

 




