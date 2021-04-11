---
description: Ruft das Menü Handle für das aktuelle Fenster ab.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: MN_GETHMENU Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216079"
---
# <a name="mn_gethmenu-message"></a>MN \_ gethmenu-Meldung

Ruft das Menü Handle für das aktuelle Fenster ab.


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HMENU**

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert das **HMENU** für das aktuelle Fenster. Wenn dies nicht möglich ist, ist der Rückgabewert **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 




