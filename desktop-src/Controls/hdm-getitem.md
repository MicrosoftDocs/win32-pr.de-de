---
title: HDM_GETITEM Meldung (Commctrl.h)
description: Ruft Informationen zu einem Element in einem Headersteuerelement ab. Sie können diese Nachricht explizit senden oder das \_ Header-GetItem-Makro verwenden.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- HDM_GETITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 566f8b8e3bdf4e92abfb1fdd5874b8514814792e1d7aae169cc2aca4b2e8d101
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436190"
---
# <a name="hdm_getitem-message"></a>HDM \_ GETITEM-Nachricht

Ruft Informationen zu einem Element in einem Headersteuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ Header-GetItem-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, für das Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDITEM-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-hditema) Wenn die Nachricht gesendet wird, gibt der **Maskenmember** den Typ der angeforderten Informationen an. Wenn die Nachricht zurückgegeben wird, erhalten die anderen Member die angeforderten Informationen. Wenn der **Maskenmember** 0 (null) angibt, gibt die Nachricht **TRUE** zurück, kopiert jedoch keine Informationen in die Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Wenn das HDI \_ TEXT-Flag im **Maskenmember** der [**HDITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-hditema) festgelegt ist, kann das Steuerelement den **pszText-Member** der -Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text aufzufüllen. Anwendungen sollten nicht davon ausgehen, dass der Text immer im angeforderten Puffer platziert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDM \_ GETITEMW** (Unicode) und **HDM \_ GETITEMA** (ANSI)<br/>                   |



 

 





