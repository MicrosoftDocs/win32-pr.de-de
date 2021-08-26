---
title: LVM_GETINSERTMARK-Nachricht (Commctrl.h)
description: Ruft die Position der Einfügemarke ab.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- LVM_GETINSERTMARK Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e64281ccc9d4638353ddbb6062ce5cf1c0a678e009639dcc43cd0d4cf52741
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002670"
---
# <a name="lvm_getinsertmark-message"></a>LVM \_ GETINSERTMARK-Nachricht

Ruft die Position der Einfügemarke ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK-Struktur,</a> die die Position der Einfügemarke empfängt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.** **FALSE** wird zurückgegeben, wenn die Größe im **cbSize-Member** der [**LVINSERTMARK-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) nicht der tatsächlichen Größe der Struktur entspricht.

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



 

 





