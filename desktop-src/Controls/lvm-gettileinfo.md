---
title: LVM_GETTILEINFO Meldung (Commctrl.h)
description: Ruft Informationen zu einer Kachel in einem Listenansicht-Steuerelement ab.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- LVM_GETTILEINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8141b3a39c47966348dfd823b557c1b0af4cca84a90ba979a358d6ac0eaa4757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079034"
---
# <a name="lvm_gettileinfo-message"></a>LVM \_ GETTILEINFO-Nachricht

Ruft Informationen zu einer Kachel in einem Listenansicht-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO-Struktur,**</a> die die abgerufenen Informationen empfängt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Rückgabewert nicht verwendet.

## <a name="remarks"></a>Hinweise

Die Kachelansicht ist eine neue Möglichkeit zum Anordnen und Anzeigen von Elementen in einem Listenansichtssteuerelement. Die anderen Ansichten sind Symbol, kleines Symbol, Details und Liste.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





