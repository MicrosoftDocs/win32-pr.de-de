---
title: TB_INSERTBUTTON Meldung (Commctrl.h)
description: Fügt eine Schaltfläche in eine Symbolleiste ein.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909a4e039450e001757cd054cf27a15d24af392d6a55841c2857e2312252145c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829651"
---
# <a name="tb_insertbutton-message"></a>TB \_ INSERTBUTTON-Nachricht

Fügt eine Schaltfläche in eine Symbolleiste ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index einer Schaltfläche. Die Meldung fügt die neue Schaltfläche links neben dieser Schaltfläche ein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TBBUTTON-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) die Informationen über die einzufügende Schaltfläche enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TB \_ INSERTBUTTONW** (Unicode) und **TB \_ INSERTBUTTONA** (ANSI)<br/>           |



 

 





