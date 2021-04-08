---
title: CB_GETCOUNT Meldung (Winuser. h)
description: Ruft die Anzahl der Elemente im Listenfeld eines Kombinations Felds ab.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- Windows-Steuerelemente für CB_GETCOUNT Meldung
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
ms.openlocfilehash: 7900aadf3ba87cc7603a3fe15f4974911c9f9a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744017"
---
# <a name="cb_getcount-message"></a>CB \_ GetCount-Nachricht

Ruft die Anzahl der Elemente im Listenfeld eines Kombinations Felds ab.

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

Der Rückgabewert ist die Anzahl der Elemente im Listenfeld. Wenn ein Fehler auftritt, ist es CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Der Index ist NULL basiert, sodass die zurückgegebene Anzahl einen Wert größer als der Indexwert des letzten Elements ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



 

 





