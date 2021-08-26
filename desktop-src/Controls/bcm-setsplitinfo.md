---
title: BCM_SETSPLITINFO Nachricht (Commctrl.h)
description: Legt Informationen für ein Steuerelement für geteilte Schaltflächen fest. Senden Sie diese Nachricht explizit oder mithilfe des Button \_ SetSplitInfo-Makros.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- BCM_SETSPLITINFO Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17332ce5f10fa612d739598222e4973000961435fa525190a650adaa9aa9fc4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921420"
---
# <a name="bcm_setsplitinfo-message"></a>BCM \_ SETSPLITINFO-Nachricht

Legt Informationen für ein Steuerelement für geteilte Schaltflächen fest. Senden Sie diese Nachricht explizit oder mithilfe des [**Button \_ SetSplitInfo-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**BUTTON \_ SPLITINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) die Informationen über die unterteilte Schaltfläche enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Meldung nur mit den Schaltflächenstilen [**BS \_ SPLITBUTTON**](button-styles.md) und [**BS \_ DEFSPLITBUTTON.**](button-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





