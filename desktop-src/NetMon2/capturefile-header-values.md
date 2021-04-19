---
description: Definiert die Struktur der Netzwerkmonitor-Header Datei.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: CAPTUREFILE_HEADER_VALUES Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPTUREFILE_HEADER_VALUES
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2597b3f83a65dafd2da0198aade5243acc1184fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356704"
---
# <a name="capturefile_header_values-structure"></a>Capturefile- \_ Header \_ Werte-Struktur

Die **capturefile- \_ Header \_ Werte** Struktur definiert die Struktur der Netzwerkmonitor-Header Datei.

## <a name="syntax"></a>Syntax


```C++
typedef struct _CAPTUREFILE_HEADER_VALUES {
  DWORD      Signature;
  BYTE       BCDVerMinor;
  BYTE       BCDVerMajor;
  WORD       MacType;
  SYSTEMTIME TimeStamp;
  DWORD      FrameTableOffset;
  DWORD      FrameTableLength;
  DWORD      UserDataOffset;
  DWORD      UserDataLength;
  DWORD      CommentDataOffset;
  DWORD      CommentDataLength;
  DWORD      StatisticsOffset;
  DWORD      StatisticsLength;
  DWORD      NetworkInfoOffset;
  DWORD      NetworkInfoLength;
  DWORD      ConversationStatsOffset;
  DWORD      ConversationStatsLength;
} CAPTUREFILE_HEADER_VALUES, *LPCAPTUREFILE_HEADER_VALUES;
```



## <a name="members"></a>Member

<dl> <dt>

**Signature**
</dt> <dd>

Eindeutiger Bezeichner: ' gmbu.

</dd> <dt>

**Bcdverminor**
</dt> <dd>

Binary, Coded Decimal (Minor). Der Wert dieses Members sollte NULL (0) sein.

</dd> <dt>

**Bcdvermajor**
</dt> <dd>

Binary Coded Decimal (Major). Dieser Wert sollte 2 lauten.

</dd> <dt>

**MacType**
</dt> <dd>

Topologietyp.

</dd> <dt>

**Zeitstempel**
</dt> <dd>

Erfassungs Zeit.

</dd> <dt>

**Frametableoffset**
</dt> <dd>

Tabelle für Frame index.

</dd> <dt>

**Frametablelength**
</dt> <dd>

Tabellengröße für Frame index.

</dd> <dt>

**Userdataoffset**
</dt> <dd>

Offset von Benutzerdaten.

</dd> <dt>

**User DATALENGTH**
</dt> <dd>

Benutzerdaten Länge.

</dd> <dt>

**Commentdataoffset**
</dt> <dd>

Kommentar Daten Offset.

</dd> <dt>

**Commentdatalength**
</dt> <dd>

Länge der Kommentar Daten.

</dd> <dt>

**Statisticsoffset**
</dt> <dd>

Offset zur **Statistik** Struktur.

</dd> <dt>

**Statisticslength**
</dt> <dd>

Länge der **Statistik** Struktur.

</dd> <dt>

**Networkinfooffset**
</dt> <dd>

Offset zur **networkinfo** -Struktur.

</dd> <dt>

**Networkinfolength**
</dt> <dd>

Länge der **networkinfo** -Struktur.

</dd> <dt>

**Conversationstatusoffset**
</dt> <dd>

Dieser Member wird nicht verwendet.

</dd> <dt>

**Conversationstatuslength**
</dt> <dd>

Dieser Member wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




