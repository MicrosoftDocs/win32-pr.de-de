---
description: Die providor \_ Info \_ 2-Struktur fügt einen Druckanbieter an die Auftragsliste des Druck Anbieters an.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: PROVIDOR_INFO_2 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350827"
---
# <a name="providor_info_2-structure"></a>Providor \_ Info \_ 2-Struktur

Die **providor \_ Info \_ 2** -Struktur fügt einen Druckanbieter an die Auftragsliste des Druck Anbieters an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**Porder**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Druck Anbieters angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird beim Aufrufen von [**addprintprovidor**](addprintprovidor.md), Ebene 2, zum Hinzufügen des angegebenen Druck Anbieters am Ende der Auftragsliste des Druck Anbieters verwendet. Der Anbieter wird sofort für das Routing verwendet, wenn der-Befehl erfolgreich ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Providor \_ Info \_ 2W** (Unicode) und **\_ providor \_ Info \_ 2a** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprintprovidor**](addprintprovidor.md)
</dt> </dl>

 

 




