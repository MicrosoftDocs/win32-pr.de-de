---
title: LVM_SORTGROUPS Meldung (Commctrl.h)
description: Verwendet eine anwendungsdefinierte Vergleichsfunktion, um Gruppen nach ID innerhalb eines Listenansichtssteuerelements zu sortieren.
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ec17d46205746495cfe95a2af83690644dd8bfced26041906bdea4f809fb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670784"
---
# <a name="lvm_sortgroups-message"></a>LVM \_ SORTGROUPS-Nachricht

Verwendet eine anwendungsdefinierte Vergleichsfunktion, um Gruppen nach ID innerhalb eines Listenansichtssteuerelements zu sortieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Zeiger auf eine anwendungsdefinierte Vergleichsfunktion, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare.</a></dd> <dt>

*lParam* 
</dt> <dd>Void-Zeiger auf die anwendungsdefinierte Information.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 1 zurück, andernfalls 0.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

