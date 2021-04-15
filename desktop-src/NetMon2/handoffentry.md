---
description: Die handoffentry-Struktur definiert einen bestimmten Protokolleintrag in einer handofftable-Struktur.
ms.assetid: 85793326-3007-4dd9-9325-3447d6e09883
title: Handoffentry-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7c04c7bc90fdd0f36beb6aed26a6b84c077eff5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525127"
---
# <a name="handoffentry-structure"></a>Handoffentry-Struktur

Die **handoffentry** -Struktur definiert einen bestimmten Protokolleintrag in einer **handofftable** -Struktur.

Diese Struktur wird von Netzwerkmonitor basierend auf Informationen in einer vom Benutzer bereitgestellten ini-Datei ausgefüllt, die beim Aufrufen der [**createhandofftable**](createhandofftable.md) -Funktion bereitgestellt wird. Diese Struktur sollte nie explizit von einer Anwendung geändert werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct _SESSIONSTATS {
  DWORD      hoe_sig;
  DWORD      hoe_ProtIdentNumber;
  HPPROTOCOL hoe_ProtocolHandle;
  DWORD      hoe_ProtocolData;
} HANDOFFENTRY, *LPHANDOFFENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**Hacke \_ sig**
</dt> <dd>

Die Signatur, die diesen Eintrag als einen Übergabe Tabelleneintrag bezeichnet.

</dd> <dt>

**Hacke- \_ protidentnumber**
</dt> <dd>

Von der vom Benutzer bereitgestellte ini-Datei bereitgestellte Protokollnummer.

</dd> <dt>

**Hacken- \_ protocolhandle**
</dt> <dd>

Protokoll handle, das mithilfe des Protokoll namens erstellt wird, der von der vom Benutzer bereitgestellten ini-Datei bereitgestellt

</dd> <dt>

**\_protocoldata hacken**
</dt> <dd>

Protokollinstanzdaten, die von der vom Benutzer bereitgestellten ini-Datei

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von Netzwerkmonitor ausgefüllt, wenn Netzwerkmonitor eine Übergabe Tabelle erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Handofftable](handofftable.md)
</dt> </dl>

 

 




