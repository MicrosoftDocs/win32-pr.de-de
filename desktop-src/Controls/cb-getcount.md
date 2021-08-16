---
title: CB_GETCOUNT (Winuser.h)
description: Ruft die Anzahl der Elemente im Listenfeld eines Kombinationsfelds ab.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- CB_GETCOUNT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215046ae9558fd03388b2b0637233c2f69832ea07a7f20fd24ddc0a5eb3c177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832278"
---
# <a name="cb_getcount-message"></a>CB \_ GETCOUNT-Nachricht

Ruft die Anzahl der Elemente im Listenfeld eines Kombinationsfelds ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl der Elemente im Listenfeld. Wenn ein Fehler auftritt, ist dies CB \_ ERR.

## <a name="remarks"></a>Hinweise

Der Index ist nullbasierte, sodass die zurückgegebene Anzahl um eins größer als der Indexwert des letzten Elements ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



 

 





