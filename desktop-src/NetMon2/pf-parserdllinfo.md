---
description: Die PF \_ parserdllinfo-Struktur definiert die Parser, die sich in der Parser-DLL befinden.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: PF_PARSERDLLINFO Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERDLLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ab4a3673c567a72cb5d0284a07d5603913e77550
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960143"
---
# <a name="pf_parserdllinfo-structure"></a>PF- \_ parameserdllinfo-Struktur

Die **PF \_ parserdllinfo** -Struktur definiert die Parser, die sich in der Parser-DLL befinden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**nparser**
</dt> <dd>

Anzahl der Parser in der Parser-DLL.

</dd> <dt>

**"Parser Info"**
</dt> <dd>

Array von [PF \_ parserinfo](pf-parserinfo.md) -Strukturen, die jeden Parser in der Parser-DLL beschreiben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **PF \_ parserdllinfo** -Struktur wird von der [parserautoinstallinfo](parserautoinstallinfo.md) -Exportfunktion zurückgegeben, die in der Parser-DLL implementiert ist. Die **parserautoinstallinfo** -Funktion identifiziert die Anzahl der Parser in der dll und verwendet ein Array von [PF \_ parserinfo](pf-parserinfo.md) -Strukturen, um die einzelnen Parser zu beschreiben.

Die PF \_ parserdllinfo-Struktur muss mithilfe von **heapzuc** zugeordnet werden.



| Für Informationen zu                                               | Siehe                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.        | [Parser](parsers.md)                                                      |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.               | [Architektur der Parser-DLL](parser-dll-architecture.md)                      |
| Zum Implementieren von " **Parser autoinstallinfo**  " ist ein Beispiel enthalten. | [Implementieren von "Parser autoistallinfo"](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PF-Parameter \_ Info](pf-parserinfo.md)
</dt> <dt>

["Parameserautoinstallinfo"](parserautoinstallinfo.md)
</dt> </dl>

 

 




