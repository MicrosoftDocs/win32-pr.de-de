---
description: Der LARGEINT-Datentyp definiert einen LARGE \_ INTEGER-Wert.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: LARGEINT (Netmon.h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6eedf739d9d0b4285d0198ae905672dbbb7848a2b7d9ba106abb6a59fcdc4d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742650"
---
# <a name="largeint"></a>LARGEINT

Der **LARGEINT-Datentyp** definiert einen [**LARGE \_ INTEGER-Wert.**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Hinweise

Der **lpLargeIntTable-Member** der [**SET-Struktur**](set.md) zeigt auf ein Array von **SET-Strukturen,** die einen oder mehrere LARGEINT-Werte definieren. Wenn dieser **Set-Strukturtyp** angegeben wird, zeigt Netzwerkmonitor eine der folgenden Bezeichnungen mit jedem LARGEINT-Wert an, den sie im Protokollpaket findet.

-   Entspricht dem festgelegten Wert. Der LARGEINT-Wert ist in der Menge enthalten.
-   Unbekannter festgelegter Wert. Der LARGEINT-Wert ist nicht in der Menge enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

