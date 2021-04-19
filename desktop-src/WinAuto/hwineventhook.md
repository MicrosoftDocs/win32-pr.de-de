---
title: Hwineventhook (WINDEF. h)
description: Wird verwendet, um eine Windows Event Hook-Funktion zu deklarieren.
ms.assetid: fa193e8e-46a8-46d4-83e1-e6274276b218
keywords:
- Hwineventhook
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf526846916dfdd701f4f5ee98778dbbe9e66d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341610"
---
# <a name="hwineventhook"></a>Hwineventhook

Wird verwendet, um eine Windows Event Hook-Funktion zu deklarieren.


```C++
typedef HANDLE HWINEVENTHOOK;
```



## <a name="remarks"></a>Bemerkungen

Dieser Datentyp wird mit der [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) -Rückruffunktion und den Funktionen [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) und [**unhookwinevent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                                          |
| Verteilbare Komponente<br/>          | Active Accessibility 1,3 RDK unter Windows NT 4,0 mit SP6 und höher und Windows 95<br/>                                   |
| Header<br/>                   | <dl> <dt>WINDEF. h (winver >= 0x0500) (Include Windows. h)</dt> </dl> |



 

 





