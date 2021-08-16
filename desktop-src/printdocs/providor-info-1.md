---
description: Die PROVIDOR \_ INFO \_ 1-Struktur identifiziert einen Druckanbieter.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: PROVIDOR_INFO_1 -Struktur (Winspool.h)
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
ms.openlocfilehash: 4f9e7015382ef34f4582c4772e148059c4ed01de9e81da5af71bc0849df26f15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091700"
---
# <a name="providor_info_1-structure"></a>PROVIDOR \_ INFO \_ 1-Struktur

Die **PROVIDOR \_ INFO \_ 1-Struktur** identifiziert einen Druckanbieter.

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

Zeiger auf eine auf NULL beendete Zeichenfolge, die der Name des Druckanbieters ist.

</dd> <dt>

**pUmgebung**
</dt> <dd>

Zeiger auf eine auf NULL beendete Umgebungszeichenfolge, die die Umgebung angibt, in der die Dynamic Link Library (DLL) des Anbieters ausgeführt werden soll.

</dd> <dt>

**pDLLName**
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge, die der Name des Anbieters .dll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **\_ PROVIDOR \_ INFO \_ 1W** (Unicode) und **\_ PROVIDOR \_ INFO \_ 1A** (ANSI)<br/>                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Drucken von Spooler-API-Strukturen](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




