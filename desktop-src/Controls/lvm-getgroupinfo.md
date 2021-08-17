---
title: LVM_GETGROUPINFO-Nachricht (Commctrl.h)
description: Ruft Gruppeninformationen ab.
ms.assetid: 72d84e0b-121e-473b-a34d-874234c598b6
keywords:
- LVM_GETGROUPINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5c48a21a1bba0c6dd1af3fd567ea853dc922591c553ea11a935fb705ad65bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411394"
---
# <a name="lvm_getgroupinfo-message"></a>LVM \_ GETGROUPINFO-Meldung

Ruft Gruppeninformationen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Eine ID, die die Gruppe angibt, deren Informationen abgerufen werden.</dd> <dt>

*lParam* 
</dt> <dd>Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP-Struktur,**</a> die die abgerufenen Informationen empfängt. Legen Sie den **cbSize-Member** dieser Struktur auf sizeof(LVGROUP) fest. </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die ID der Gruppe zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Bevor Sie versuchen, den Header für eine Gruppe abzurufen, stellen Sie zunächst sicher, dass die Gruppe nicht über den \_ LBGS NOHEADER-Stil verfügt.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





