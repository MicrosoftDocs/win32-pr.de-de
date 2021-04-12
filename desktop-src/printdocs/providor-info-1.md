---
description: Die providor \_ Info \_ 1-Struktur identifiziert einen Druckanbieter.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: PROVIDOR_INFO_1 Struktur (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347488"
---
# <a name="providor_info_1-structure"></a>Providor \_ Info \_ 1-Struktur

Die **providor \_ Info \_ 1** -Struktur identifiziert einen Druckanbieter.

## <a name="syntax"></a>Syntax


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a>Member

<dl> <dt>

**pName**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des Druck Anbieters ist.

</dd> <dt>

**nach-oben**
</dt> <dd>

Zeiger auf eine mit NULL endenden Umgebungs Zeichenfolge, die die Umgebung angibt, in der die Anbieter-DLL (Dynamic-Link Library) ausgeführt werden soll.

</dd> <dt>

**pdllname**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die der Name der Anbieter. dll ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ Providor \_ Info \_ 1W** (Unicode) und **\_ providor \_ Info \_ 1a** (ANSI)<br/>                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druck Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**Addprintprovidor**](addprintprovidor.md)
</dt> </dl>

 

 




