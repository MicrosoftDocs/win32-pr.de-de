---
description: Definiert die Netzwerkmonitor Headerdateistruktur.
ms.assetid: 944980c9-ebaa-4042-a112-d32b7a28ba21
title: CAPTUREFILE_HEADER_VALUES-Struktur (Netmon.h)
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
ms.openlocfilehash: 29ee0ab0a9a927b3860760877457735198465b7c28789a542c040fc9e9e788a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367416"
---
# <a name="capturefile_header_values-structure"></a>CAPTUREFILE \_ HEADER \_ VALUES-Struktur

Die **CAPTUREFILE \_ HEADER \_ VALUES-Struktur** definiert die Netzwerkmonitor Headerdateistruktur.

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

Eindeutiger Bezeichner: 'GMBU.

</dd> <dt>

**BCDVerMinor**
</dt> <dd>

Binär, codierte Dezimalzahl (Nebenversion). Der Wert dieses Members sollte 0 (null) sein.

</dd> <dt>

**BCDVerMajor**
</dt> <dd>

Binär codierte Dezimalzahl (Hauptzeichen). Dieser Wert sollte 2 sein.

</dd> <dt>

**MacType**
</dt> <dd>

Topologietyp.

</dd> <dt>

**Timestamp**
</dt> <dd>

Zeitpunkt der Erfassung.

</dd> <dt>

**FrameTableOffset**
</dt> <dd>

Rahmenindextabelle.

</dd> <dt>

**FrameTableLength**
</dt> <dd>

Größe der Frameindextabelle.

</dd> <dt>

**UserDataOffset**
</dt> <dd>

Benutzerdatenoffset.

</dd> <dt>

**UserDataLength**
</dt> <dd>

Länge der Benutzerdaten.

</dd> <dt>

**CommentDataOffset**
</dt> <dd>

Kommentardatenoffset.

</dd> <dt>

**CommentDataLength**
</dt> <dd>

Länge der Kommentardaten.

</dd> <dt>

**StatisticsOffset**
</dt> <dd>

Offset zur **STATISTICS-Struktur.**

</dd> <dt>

**StatisticsLength**
</dt> <dd>

Länge der **STATISTICS-Struktur.**

</dd> <dt>

**NetworkInfoOffset**
</dt> <dd>

Offset zur **NETWORKINFO-Struktur.**

</dd> <dt>

**NetworkInfoLength**
</dt> <dd>

Länge der **NETWORKINFO-Struktur.**

</dd> <dt>

**ConversationStatsOffset**
</dt> <dd>

Dieser Member wird nicht verwendet.

</dd> <dt>

**ConversationStatsLength**
</dt> <dd>

Dieser Member wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




