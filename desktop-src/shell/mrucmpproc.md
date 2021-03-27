---
description: Wird verwendet, um zu bestimmen, ob ein Element in einer zuletzt verwendeten (MRU-) Liste vorhanden ist.
title: Mrucmpproc-Rückruffunktion
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
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959124"
---
# <a name="mrucmpproc-callback-function"></a>Mrucmpproc-Rückruffunktion

Wird verwendet, um zu bestimmen, ob ein Element in einer zuletzt verwendeten (MRU-) Liste vorhanden ist.

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

Gibt 0 zurück, wenn die Elemente identisch sind, andernfalls ein Wert ungleich 0 (null).

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann optional für die Verwendung in der [**mruinfo**](mruinfo.md) -Struktur angegeben werden, die an " [**kreatemrulistw**](createmrulist.md)" übergeben wird. Dies ist hilfreich, wenn die MRU-Liste mit dem **MRU- \_ Binärflag** erstellt wurde. Wenn diese Funktion nicht angegeben wird, werden standardmäßige Zeichen folgen Vergleichsfunktionen verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>      |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>            |
| Unicode- und ANSI-Name<br/>   | **Mrucmpprocw** (Unicode) und **mrucmpproca** (ANSI)<br/> |



 

 




