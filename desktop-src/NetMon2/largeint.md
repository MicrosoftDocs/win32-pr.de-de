---
description: Der largeint-Datentyp definiert einen großen \_ ganzzahligen Wert.
ms.assetid: 65801136-bde7-4bca-af1f-243e757f3d8d
title: Largeint (Netmon. h)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d857179e97586974e11815ced5ec7c50ca276789
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345940"
---
# <a name="largeint"></a>' Largeint

Der **largeint** -Datentyp definiert einen [**großen \_ ganzzahligen**](/windows/win32/api/winnt/ns-winnt-large_integer-r1) Wert.


```C++
typedef LARGE_INTEGER* LPLARGEINT;
typedef LARGE_INTEGER UNALIGNED* ULPLARGEINT;
```



## <a name="remarks"></a>Bemerkungen

Der **lplargein-** Member der [**set**](set.md) -Struktur verweist auf ein Array von **set** -Strukturen, die einen oder mehrere largeint-Werte definieren. Wenn diese Art von **Set** -Struktur angegeben ist, zeigt Netzwerkmonitor eine der folgenden Bezeichnungen mit jedem largeint-Wert an, der im Protokoll Paket gefunden wird.

-   Entspricht dem Satz Wert. Der largeint-Wert ist im Satz enthalten.
-   Unbekannter festgelegtem Wert. Der largeint-Wert ist nicht in der Gruppe enthalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SET](set.md)
</dt> </dl>

 

