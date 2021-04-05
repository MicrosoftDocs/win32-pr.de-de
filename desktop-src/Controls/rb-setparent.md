---
title: RB_SETPARENT Meldung (kommstrg. h)
description: Legt das übergeordnete Fenster eines Info leisten Steuer Elements fest.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- Windows-Steuerelemente für RB_SETPARENT Meldung
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859067"
---
# <a name="rb_setparent-message"></a>RB- \_ SetParent-Nachricht

Legt das übergeordnete Fenster eines Info leisten Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Handle für das übergeordnete Fenster, das festgelegt werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das vorherige übergeordnete Fenster zurück, oder **null** , wenn kein vorheriges übergeordnetes Element vorhanden ist.

## <a name="remarks"></a>Bemerkungen

Das Grund leisten-Steuerelement sendet Benachrichtigungs Meldungen an das Fenster, das Sie mit dieser Meldung angeben. Mit dieser Meldung wird das übergeordnete Element des Grund leisten-Steuer Elements nicht geändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





