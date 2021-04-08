---
title: Struktur "netwheader"
description: Enthält die Anzahl der Symbol-oder Cursor Komponenten in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- Menüs für die netwheader-Struktur und weitere Ressourcen
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949554"
---
# <a name="newheader-structure"></a>Struktur "netwheader"

Enthält die Anzahl der Symbol-oder Cursor Komponenten in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**Reserved**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Bleiben muss 0 (null) sein.

</dd> <dt>

**RESTYPE**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Ressourcentyp. Dieser Member muss einen der folgenden Werte aufweisen.



| Wert                                                                                                                                                                                                       | Bedeutung                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <dt>**Res \_ Cursor**</dt> <dt>2</dt> </dl> | Der Cursor Ressourcentyp.<br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <dt>**Res \_ Symbol**</dt> <dt>1</dt> </dl>       | Symbol Ressourcentyp.<br/>   |



 

</dd> <dt>

**Rescount**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der Symbol-oder Cursor Komponenten in der Ressourcengruppe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine oder mehrere [**resdir**](resdir.md) -Strukturen folgen direkt der Struktur " **netwheader** " in der RES-Datei. Der **rescount** -Member gibt die Anzahl der **resdir** -Strukturen an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Resdir**](resdir.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





