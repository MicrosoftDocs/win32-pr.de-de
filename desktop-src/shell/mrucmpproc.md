---
description: Wird verwendet, um zu bestimmen, ob ein Element in einer LISTE der zuletzt verwendeten Elemente (MRU) vorhanden ist.
title: MRUCMPPROC-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840781"
---
# <a name="mrucmpproc-callback-function"></a>MRUCMPPROC-Rückruffunktion

Wird verwendet, um zu bestimmen, ob ein Element in einer LISTE der zuletzt verwendeten Elemente (MRU) vorhanden ist.

## <a name="syntax"></a>Syntax


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pString1* 
</dt> <dd>

Typ: **LPCTSTR**

Die erste Zeichenfolge.

</dd> <dt>

*pString2* 
</dt> <dd>

Typ: **LPCTSTR**

Eine zweite Zeichenfolge, die mit der ersten verglichen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **int**

Gibt 0 zurück, wenn die Elemente identisch sind, andernfalls ein Wert ungleich 0.

## <a name="remarks"></a>Hinweise

Diese Funktion kann optional für die Verwendung in der [**MRUINFO-Struktur**](mruinfo.md) angegeben werden, die an [**CreateMRUListW übergeben wird.**](createmrulist.md) Dies ist nützlich, wenn die MRU-Liste mit dem **MRU \_ BINARY-Flag erstellt** wurde. Wenn diese Funktion nicht angegeben wird, werden Standardfunktionen für den Zeichenfolgenvergleich verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>            |
| Unicode- und ANSI-Name<br/>   | **MRUCMPPROCW** (Unicode) und **MRUCMPPROCA** (ANSI)<br/> |



 

 




