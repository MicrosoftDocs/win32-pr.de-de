---
title: LVM_INSERTMARKHITTEST (Commctrl.h)
description: Ruft die Einfügemarke ab, die einer angegebenen Stelle am nächsten ist.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST von Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250585fea10846e10238132c5150f5ace9f8e00c474e763023c36c8566fbc752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919980"
---
# <a name="lvm_insertmarkhittest-message"></a>LVM \_ INSERTMARKHITTEST-Meldung

Ruft die Einfügemarke ab, die einer angegebenen Stelle am nächsten ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Zeiger auf eine **POINT-Struktur,** die die Treffertestkoordinaten enthält.</dd> <dt>

*lParam* 
</dt> <dd>Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK-Struktur,</a> die die Einfügemarke angibt, die den durch den *wParam-Parameter* definierten Koordinaten am nächsten kommt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.** **FALSE** wird zurückgegeben, wenn die Größe im **cbSize-Member** der [**LVINSERTMARK-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) nicht der tatsächlichen Größe der Struktur entspricht, oder wenn eine Einfügemarke in der aktuellen Ansicht nicht angewendet wird.

## <a name="remarks"></a>Hinweise

Eine Einfügemarke kann nur angezeigt werden, wenn sich das Listenansicht-Steuerelement in der Symbolansicht, kleinen Symbolansicht oder Kachelansicht befindet und sich nicht im Gruppenansichtsmodus befindet.

Wenn Einfügepunkte nicht für die Ansicht gelten, enthält die [**LVINSERTMARK-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) im **iItem-Member eine** -1.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll 6.0 an. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





