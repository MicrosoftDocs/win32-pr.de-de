---
description: Die PF \_ PARSERINFO-Struktur definiert jeweils einen Parser. In der PF \_ PARSERINFO-Struktur wird ein Parser durch die Informationen über das Protokoll definiert, das der Parser erkennt.
ms.assetid: e1180952-9560-4386-9320-919dfb8171b3
title: PF_PARSERINFO-Struktur (Netmon.h)
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
ms.openlocfilehash: 533e8dae6a009488998acd3232b062b423553b9df10f14ec97ef9ae2f8c55bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889940"
---
# <a name="pf_parserinfo-structure"></a>PF \_ PARSERINFO-Struktur

Die **PF \_ PARSERINFO-Struktur** definiert jeweils einen Parser. In der **PF \_ PARSERINFO-Struktur** wird ein Parser durch die Informationen über das Protokoll definiert, das der Parser erkennt.

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

**szProtocolName**
</dt> <dd>

Der Name des Protokolls, das der Parser erkennt.

</dd> <dt>

**szComment**
</dt> <dd>

Kurze Beschreibung des Protokolls.

</dd> <dt>

**szHelpFile**
</dt> <dd>

Name der Protokollhilfedatei, falls vorhanden.

</dd> <dt>

**pWhoCanPrecedeMe**
</dt> <dd>

Zeiger auf eine [PF \_ FOLLOWSET-Struktur,](pf-followset.md) die die Protokolle auflistet, die dem Protokoll vorangestellt werden können, das die **PF \_ PARSERINFO-Struktur** beschreibt. Netzwerkmonitor fügt das Parserprotokoll dem [*folgenden Satz*](f.md) aller Protokolle im Satz hinzu.

</dd> <dt>

**pWhoCanFollowMe**
</dt> <dd>

Zeiger auf eine [PF \_ FOLLOWSET-Struktur,](pf-followset.md) die das Protokoll auflistet, das dem Protokoll folgen kann, das in der **PF \_ PARSERINFO-Struktur** beschrieben wird. Netzwerkmonitor fügt die Protokolle des Satzes dem [*folgenden Satz*](f.md) des Parserprotokolls hinzu.

</dd> <dt>

**pWhoHandsOffToMe**
</dt> <dd>

Zeiger auf eine [PF \_ HANDOFFSET-Struktur,](pf-handoffset.md) die an das Protokoll weitergibt, das von der **PF \_ PARSERINFO-Struktur** beschrieben wird. Netzwerkmonitor fügt das Parserprotokoll den [*Übergabesätzen*](h.md) aller Protokolle im Satz hinzu.

</dd> <dt>

**pWhoDoIHandOffTo**
</dt> <dd>

Zeiger auf eine [PF \_ HANDOFFSET-Struktur,](pf-handoffset.md) die die Protokolle auflistet, an die das Parserprotokoll übergeben wird. Netzwerkmonitor fügt die Protokolle dieses Satzes dem [*Übergabesatz*](h.md) des Parserprotokolls hinzu.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **PF \_ PARSERINFO-Struktur** wird in der **PF \_ PARSERDLLINFO-Struktur** verwendet, um eine Beschreibung eines Parsers bereitzustellen. Netzwerkmonitor verwendet die Parserbeschreibung, um die [*Parser.ini-Datei*](p.md) und die INI-Dateien der Parser zu aktualisieren, die dem in der **PF \_ PARSERINFO-Struktur** beschriebenen Protokoll vorangehen und diesem folgen.

Ein Folgesatz gibt die Protokolle an, die einem Protokoll folgen. Netzwerkmonitor verwendet einen Folgesatz, wenn der Parser das nächste Protokoll nicht anhand der Daten in einer Protokollinstanz identifizieren kann. Ein Folgesatz wird in der [*dateiParser.ini*](p.md) gespeichert. Wenn der Parser zum ersten Mal installiert wird, aktualisiert Netzwerkmonitor den folgenden Satz von Parserprotokollen, die in **pWhoCanPrecedeMe** und **pWhoCanFollowMe** aufgeführt sind.

Ein Übergabesatz gibt die Protokolle an, die einem Protokoll folgen. Der Parser verwendet einen Übergabesatz nur, wenn der Parser das nächste Protokoll aus den Daten in einer Protokollinstanz identifizieren kann. Ein Übergabesatz wird in den INI-Dateien jedes Parsers gespeichert. Wenn der Parser zum ersten Mal installiert wird, aktualisiert Netzwerkmonitor den Übergabesatz der Parserprotokolle, die in **pWhoHandsOffToMe** und **pWhoDoIHandOffTo** aufgeführt sind.



| Für Informationen zu                                               | Siehe                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor arbeiten.        | [Parser](parsers.md)                                                       |
| Die folgenden Sätze enthalten.                                        | [Angeben eines Folgesatzes](specifying-a-follow-set.md)                       |
| Welche Übergabesätze enthalten sind.                                       | [Angeben eines Übergabesatzes](specifying-a-handoff-set.md)                     |
| Welche Einstiegspunkte sind in der Parser-DLL enthalten?                | [Parser-DLL-Architektur](parser-dll-architecture.md)                       |
| Die Implementierung von **ParserAutoInstallInfo**  enthält ein Beispiel. | [Implementieren von ParserAutoInstallInfo](implementing-parserautoinstallinfo.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ParserAutoInstallInfo](parserautoinstallinfo.md)
</dt> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> <dt>

[PF \_ HANDOFFSET](pf-handoffset.md)
</dt> <dt>

[PF \_ PARSERDLLINFO](pf-parserdllinfo.md)
</dt> </dl>

 

 




