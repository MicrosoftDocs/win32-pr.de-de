---
title: LVM_GETTILEVIEWINFO (Commctrl.h)
description: Ruft Informationen zu einem Listenansicht-Steuerelement in der Kachelansicht ab.
ms.assetid: 114990c0-a150-49d8-80e7-b084c648ac34
keywords:
- LVM_GETTILEVIEWINFO meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_GETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6923f47e4a185ac036a3462a2691036573e8ddfedef9b5f9ab1327ce8204b85f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575690"
---
# <a name="lvm_gettileviewinfo-message"></a>LVM \_ GETTILEVIEWINFO-Nachricht

Ruft Informationen zu einem Listenansicht-Steuerelement in der Kachelansicht ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO-Struktur,**</a> die die abgerufenen Informationen empfängt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Rückgabewert wird nicht verwendet.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





