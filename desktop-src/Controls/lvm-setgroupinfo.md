---
title: LVM_SETGROUPINFO Meldung (Commctrl.h)
description: Legt Gruppeninformationen fest.
ms.assetid: f79bd235-e2de-4055-be3e-76eb2744e1ee
keywords:
- LVM_SETGROUPINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_SETGROUPINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553a81c3cfe962ae6daf5ae4c988964028554bc662cec08df40c16fd8b4eb43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077270"
---
# <a name="lvm_setgroupinfo-message"></a>LVM \_ SETGROUPINFO-Meldung

Legt Gruppeninformationen fest. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ SetGroupInfo-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setgroupinfo)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>ID, die die Gruppe angibt, deren Informationen festgelegt werden sollen.</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Zeiger auf eine [**LVGROUP-Struktur,**](windows/win32/api/commctrl/ns-commctrl-lvgroup) die die festzulegende Information enthält.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg die ID der Gruppe zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Um eine Gruppen-ID einer vorhandenen Gruppe zu ändern, fügen Sie <b>LVGF_GROUPID</b> zu <b>LVGROUP.mask</b> hinzu, und legen Sie <b>LVGROUP.iGroupId</b> auf die neue ID fest. Der Aufruf schlägt fehl, wenn <b>LVGROUP.iGroupId</b> die ID einer vorhandenen Gruppe enthält.

Um andere Eigenschaften einer vorhandenen Gruppe zu aktualisieren (z. B. eine Ausrichtung des Kopf- oder Fußzeilentexts für die <b>Gruppe, uAlign),</b>darf <b>LVGROUP.mask</b> keine <b>LVGF_GROUPID</b>enthalten. Andernfalls schlägt das Update fehl.

> [!Note]  
> Um diese Meldung verwenden zu können, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





