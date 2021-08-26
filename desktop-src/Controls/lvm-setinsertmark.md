---
title: LVM_SETINSERTMARK Nachricht (Commctrl.h)
description: Legt die Einfügemarke auf die definierte Position fest.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- LVM_SETINSERTMARK Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fae1cad35bd20605c4cb229dac69eb7461add8b7240b495cc48fb809d39aa098
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919860"
---
# <a name="lvm_setinsertmark-message"></a>LVM \_ SETINSERTMARK-Nachricht

Legt die Einfügemarke auf die definierte Position fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK-Struktur,</a> die angibt, wo die Einfügemarke festgelegt werden soll.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.** **FALSE** wird zurückgegeben, wenn die Größe im **cbSize-Member** der [**LVINSERTMARK-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) nicht der tatsächlichen Größe der Struktur entspricht oder wenn eine Einfügemarke in der aktuellen Ansicht nicht angewendet wird.

## <a name="remarks"></a>Hinweise

Eine Einfügemarke kann nur angezeigt werden, wenn sich das Listenansichts-Steuerelement in der Symbolansicht, der kleinen Symbolansicht oder der Kachelansicht befindet und sich nicht im Gruppenansichtsmodus befindet.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





