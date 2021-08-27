---
title: LVM_REMOVEGROUP Nachricht (Commctrl.h)
description: Entfernt eine Gruppe aus einem Listenansichtssteuerelement.
ms.assetid: c6f4f54c-4cf8-47d0-8e96-fa8a1df0501b
keywords:
- LVM_REMOVEGROUP Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_REMOVEGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c644a0367747ad63eb15a2b83a8df3078c1c89ca1c51875b178aa22d054de2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062320"
---
# <a name="lvm_removegroup-message"></a>LVM \_ REMOVEGROUP-Meldung

Entfernt eine Gruppe aus einem Listenansichtssteuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>ID, die die zu entfernende Gruppe angibt.</dd> <dt>

*lParam* 
</dt> <dd>

Muss **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index der Gruppe zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





