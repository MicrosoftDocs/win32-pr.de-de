---
description: Die handofftable-Struktur definiert die Protokolle einer Übergabe-Tabelle.
ms.assetid: 6bb7465b-c1ba-4ffe-aecf-8125993c309a
title: Handofftable-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HANDOFFTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 842ef9fde56ff6b4c420034b861aa8c151e7e6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344658"
---
# <a name="handofftable-structure"></a>Handofftable-Struktur

Die **handofftable** -Struktur definiert die Protokolle einer Übergabe-Tabelle.

Diese Struktur wird von Netzwerkmonitor basierend auf Informationen in einer vom Benutzer bereitgestellten ini-Datei ausgefüllt, die beim Aufrufen der [**createhandofftable**](createhandofftable.md) -Funktion bereitgestellt wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct HANDOFFTABLE {
  DWORD          hot_sig;
  DWORD          hot_NumEntries;
  LPHANDOFFENTRY hot_Entries;
} HANDOFFTABLE, *LPHANDOFFTABLE;
```



## <a name="members"></a>Member

<dl> <dt>

**heiße \_ sig**
</dt> <dd>

Die Signatur, die diese Tabelle als eine Übergabe Tabelle bezeichnet.

</dd> <dt>

**heiße \_ numentries**
</dt> <dd>

Anzahl von Einträgen, die der Übergabe Tabelle Netzwerkmonitor hinzugefügt wurden.

</dd> <dt>

**Hot- \_ Einträge**
</dt> <dd>

Handoff-Tabelle.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur und die zugehörigen handoffentry-Strukturen werden durch Netzwerkmonitor ausgefüllt, wenn Netzwerkmonitor eine Übergabe Tabelle erstellt.

Die Protokollinformationen, die beim Erstellen einer Übergabe Tabelle verwendet werden, werden in einer INI-Datei bereitgestellt, die von der Anwendung bereitgestellt wird, wenn " [**deehandofftable**](createhandofftable.md) " aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Handoffentry](handoffentry.md)
</dt> <dt>

["Kreatehandofftable"](createhandofftable.md)
</dt> </dl>

 

 




