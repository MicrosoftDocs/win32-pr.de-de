---
description: Die PF \_ parserinfo-Struktur definiert jeweils einen Parser. In der PF \_ parserinfo-Struktur wird ein Parser durch die Informationen über das Protokoll definiert, das der Parser erkennt.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: PF_PARSERINFO Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_PARSERINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 28ebeaad31e6f40ceb961d8c303a22590966947f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348130"
---
# <a name="pf_parserinfo-structure"></a>PF- \_ parameserinfo-Struktur

Die **PF \_ parserinfo** -Struktur definiert jeweils einen Parser. In der **PF \_ parserinfo** -Struktur wird ein Parser durch die Informationen über das Protokoll definiert, das der Parser erkennt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PF_PARSERINFO {
  char           szProtocolName[MAX_PROTOCOL_NAME_LEN];
  char           szComment[MAX_PROTOCOL_COMMENT_LEN];
  char           szHelpFile[MAX_PATH];
  PPF_FOLLOWSET  pWhoCanPrecedeMe;
  PPF_FOLLOWSET  pWhoCanFollowMe;
  PPF_HANDOFFSET pWhoHandsOffToMe;
  PPF_HANDOFFSET pWhoDoIHandOffTo;
} PF_PARSERINFO, *PPF_PARSERINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**szprotocolname**
</dt> <dd>

Der Name des Protokolls, das vom Parser erkannt wird.

</dd> <dt>

**szcomment**
</dt> <dd>

Kurze Beschreibung des Protokolls.

</dd> <dt>

**szhelpfile**
</dt> <dd>

Der Name der protokollhilfe Datei (falls vorhanden).

</dd> <dt>

**pwhocanvoran**
</dt> <dd>

Zeiger auf eine [PF \_](pf-followset.md) -nach Verfolgungs Struktur, die die Protokolle auflistet, die dem Protokoll vorangestellt sind, das die PF-Parameter **\_ Info** -Struktur beschreibt. Netzwerkmonitor fügt dem [*folgenden Satz*](f.md) aller Protokolle im Satz das parserprotokoll hinzu.

</dd> <dt>

**pwhocanfollowme**
</dt> <dd>

Zeiger auf eine [PF \_](pf-followset.md) -nach Verfolgungs Struktur, die das Protokoll auflistet, das dem Protokoll entsprechen kann, das von der PF-Parameter **\_ Info** -Struktur beschrieben wird. Netzwerkmonitor fügt die Protokolle des Satzes dem [*folgenden Satz*](f.md) des parserprotokolls hinzu.

</dd> <dt>

**pwhohandsofftome**
</dt> <dd>

Zeiger auf eine [PF- \_ handoffset](pf-handoffset.md) -Struktur, die an das Protokoll übergibt, das von der PF-Parameter **\_ Info** -Struktur beschrieben wird. Netzwerkmonitor fügt das parserprotokoll den [*Übergabe Sätzen*](h.md) aller Protokolle in der Menge hinzu.

</dd> <dt>

**pwhodoihandoffto**
</dt> <dd>

Zeiger auf eine [PF- \_ handoffset](pf-handoffset.md) -Struktur, die die Protokolle auflistet, an die das Parser-Protokoll übergibt. Netzwerkmonitor fügt die Protokolle dieses Satzes dem [*Übergabe Satz*](h.md) des parserprotokolls hinzu.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **PF \_ parserinfo** -Struktur wird in der **PF \_ parserdllinfo** -Struktur verwendet, um eine Beschreibung eines Parsers bereitzustellen. Netzwerkmonitor verwendet die parserbeschreibung, um die [*Parser.ini*](p.md) Datei zu aktualisieren, und die INI-Dateien der Parser, die vor dem in der **PF \_ parserinfo** -Struktur beschriebenen Protokoll stehen.

Ein nachfolgenden Satz gibt die Protokolle an, die einem Protokoll folgen. Netzwerkmonitor verwendet einen nachfolgenden Satz, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz nicht identifizieren kann. Ein nachfolgenden Satz wird in der [*Parser.ini*](p.md) -Datei gespeichert. Wenn der Parser zum ersten Mal installiert wird, aktualisiert Netzwerkmonitor den folgenden Satz der parserprotokolle, die in " **pwhocanvoranstellen** " und " **pwhocanfollowme**" aufgeführt sind.

Ein Übergabe-Satz gibt die Protokolle an, die einem Protokoll folgen. Der Parser verwendet einen Handzettel Satz nur dann, wenn der Parser das nächste Protokoll aus den Daten in einer Protokoll Instanz identifizieren kann. Ein Übergabe-Satz wird in den INI-Dateien der einzelnen Parser gespeichert. Wenn der Parser zum ersten Mal installiert wird, aktualisiert Netzwerkmonitor den Übergabe Satz der parserprotokolle, die in **pwhohandsofftome** und **pwhodoihandoffto** aufgeführt sind.



| Für Informationen zu                                               | Siehe                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.        | [Parser](parsers.md)                                                       |
| Die folgenden Sätze enthalten.                                        | [Angeben eines folgenden Satzes](specifying-a-follow-set.md)                       |
| Gibt an, welche Handzettel Sätze enthalten.                                       | [Angeben einer Übergabe Gruppe](specifying-a-handoff-set.md)                     |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.                | [Architektur der Parser-DLL](parser-dll-architecture.md)                       |
| Zum Implementieren von " **Parser autoinstallinfo**  " ist ein Beispiel enthalten. | [Implementieren von "parameserautoinstallinfo"](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Parameserautoinstallinfo"](parserautoinstallinfo.md)
</dt> <dt>

[PF-nach \_ Verfolgung](pf-followset.md)
</dt> <dt>

[PF- \_ handoffset](pf-handoffset.md)
</dt> <dt>

[PF- \_ Parser (Parser)](pf-parserdllinfo.md)
</dt> </dl>

 

 




