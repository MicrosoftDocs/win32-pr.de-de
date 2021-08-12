---
title: EM_SHOWBALLOONTIP Meldung (Commctrl.h)
description: Die EM \_ SHOWBALLOONTIP-Meldung zeigt eine Sprechblasentipp an, die einem Bearbeitungssteuerelement zugeordnet ist.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- EM_SHOWBALLOONTIP Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ec2666d18c0f6ce43d5c7644eca0aa2a2cc1f3af72cea03ad34af5ca451cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672323"
---
# <a name="em_showballoontip-message"></a>EM \_ SHOWBALLOONTIP-Nachricht

Die **EM \_ SHOWBALLOONTIP-Meldung** zeigt eine Sprechblasentipp an, die einem Bearbeitungssteuerelement zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**EDITBALLOONTIP-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) die Informationen über die anzuzeigende Sprechblasenspitze enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **TRUE** zurückgegeben. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest angeben, das Comclt32.dll Version 6.0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EDITBALLOONTIP**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**Bearbeiten von \_ ShowBalloonTip**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





