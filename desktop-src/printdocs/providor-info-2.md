---
description: Die PROVIDOR \_ INFO \_ 2-Struktur fügt einen Druckanbieter an die Auftragsliste des Druckanbieters an.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: PROVIDOR_INFO_2-Struktur (Winspool.h)
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
ms.openlocfilehash: 969af36fe0a64bb586fbf62912ca27c6ebba9ba0a627701e4bc57f6202bfe1b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091680"
---
# <a name="providor_info_2-structure"></a>PROVIDOR \_ INFO \_ 2-Struktur

Die **PROVIDOR \_ INFO \_ 2-Struktur** fügt einen Druckanbieter an die Auftragsliste des Druckanbieters an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a>Member

<dl> <dt>

**pOrder**
</dt> <dd>

Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des Druckanbieters angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird beim Aufrufen von [**AddPrintProvidor**](addprintprovidor.md), Ebene 2, verwendet, um den angegebenen Druckanbieter am Ende der Auftragsliste des Druckanbieters hinzuzufügen. Der Anbieter wird sofort für das Routing verwendet, wenn der Aufruf erfolgreich ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PROVIDOR \_ INFO \_ 2W** (Unicode) und **\_ PROVIDOR \_ INFO \_ 2A** (ANSI)<br/>                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




