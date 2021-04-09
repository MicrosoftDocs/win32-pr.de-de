---
title: PGM_SETCHILD Meldung (kommstrg. h)
description: Legt das enthaltene Fenster für das Pager-Steuerelement fest.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- Windows-Steuerelemente für PGM_SETCHILD Meldung
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103475"
---
# <a name="pgm_setchild-message"></a>PGM- \_ setchild-Nachricht

Legt das enthaltene Fenster für das Pager-Steuerelement fest. Mit dieser Meldung wird das übergeordnete Element des enthaltenen Fensters nicht geändert. dem Pager-Steuerelement wird nur ein Fenster Handle für den Bildlauf zugewiesen. In den meisten Fällen ist das enthaltene Fenster ein untergeordnetes Fenster. Wenn dies der Fall ist, sollte das enthaltene Fenster dem Pager-Steuerelement untergeordnet sein. Sie können diese Nachricht explizit senden oder das [**Pager-Element \_ setchild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Fenster, das enthalten sein soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert wird nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





