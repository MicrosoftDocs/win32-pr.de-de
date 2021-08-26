---
description: Die PF \_ PARSERDLLINFO-Struktur definiert die Parser, die sich in der Parser-DLL befinden.
ms.assetid: a7473b58-7767-4224-be3b-e96132d98adf
title: PF_PARSERDLLINFO -Struktur (Netmon.h)
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
ms.openlocfilehash: caaafeb9883ad514366f91f3834354fbd5ac0850400e61594a5307c4533e0960
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962850"
---
# <a name="pf_parserdllinfo-structure"></a>PF \_ PARSERDLLINFO-Struktur

Die **PF \_ PARSERDLLINFO-Struktur** definiert die Parser, die sich in der Parser-DLL befinden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_PARSERDLLINFO {
  DWORD         nParsers;
  PF_PARSERINFO ParserInfo[];
} PF_PARSERDLLINFO, *PPF_PARSERDLLINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**nParsers**
</dt> <dd>

Anzahl der Parser in der Parser-DLL.

</dd> <dt>

**ParserInfo**
</dt> <dd>

Array von [PF \_ PARSERINFO-Strukturen,](pf-parserinfo.md) die jeden Parser in der Parser-DLL beschreiben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **PF \_ PARSERDLLINFO-Struktur** wird von der [ParserAutoInstallInfo-Exportfunktion](parserautoinstallinfo.md) zurückgegeben, die in der Parser-DLL implementiert ist. Die **ParserAutoInstallInfo-Funktion** identifiziert die Anzahl der Parser in der DLL und verwendet ein Array von [PF \_ PARSERINFO-Strukturen,](pf-parserinfo.md) um jeden Parser zu beschreiben.

Die PF \_ PARSERDLLINFO-Struktur muss mithilfe von **HeapAlloc zugeordnet werden.**



| Für Informationen zu                                               | Siehe                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor.        | [Parser](parsers.md)                                                      |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.               | [Parser-DLL-Architektur](parser-dll-architecture.md)                      |
| Die Implementierung von **ParserAutoInstallInfo enthält**  ein Beispiel. | [Implementieren von ParserAutoIstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> </dl>

 

 




