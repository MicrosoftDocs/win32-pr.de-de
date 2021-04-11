---
title: HDM_GETITEM Meldung (kommstrg. h)
description: Ruft Informationen zu einem Element in einem Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das-Header \_ GetItem-Makro verwenden.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- Windows-Steuerelemente für HDM_GETITEM Meldung
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
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103778"
---
# <a name="hdm_getitem-message"></a>HDM- \_ GetItem-Nachricht

Ruft Informationen zu einem Element in einem Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das- [**Header \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements, für das Informationen abgerufen werden sollen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur. Wenn die Nachricht gesendet wird, gibt das **Masken** Element den Typ der angeforderten Informationen an. Wenn die Meldung zurückgegeben wird, erhalten die anderen Member die angeforderten Informationen. Wenn das **Masken** Element NULL angibt, gibt die Meldung **true** zurück, kopiert jedoch keine Informationen in die Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn das HDI- \_ textflag im **Mask** -Member der [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) -Struktur festgelegt ist, kann das Steuerelement den **pszText** -Member der Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text zu füllen. Anwendungen sollten nicht davon ausgehen, dass der Text immer in den angeforderten Puffer eingefügt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **HDM \_ Getitemw** (Unicode) und **HDM \_ getitema** (ANSI)<br/>                   |



 

 





