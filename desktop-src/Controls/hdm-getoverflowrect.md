---
title: HDM_GETOVERFLOWRECT Meldung (Commctrl.h)
description: Ruft das umschließende Rechteck der Überlaufschaltfläche ab, wenn der HDS \_ OVERFLOW-Stil für das Headersteuerelement festgelegt und die Überlaufschaltfläche sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des \_ Header-Makros GetOverflowRect.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- HDM_GETOVERFLOWRECT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f48088ad6c4a1d8cc5b843eeafb167f790bdd8eac06c56e6cb74e8afc18d082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047050"
---
# <a name="hdm_getoverflowrect-message"></a>HDM \_ GETOVERFLOWRECT-Nachricht

Ruft das umschließende Rechteck der Überlaufschaltfläche ab, wenn der [**HDS \_ OVERFLOW-Stil**](header-control-styles.md) für das Headersteuerelement festgelegt und die Überlaufschaltfläche sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ Header-Makros GetOverflowRect.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wird nicht verwendet. Muss Null sein.

</dd> <dt>

*lParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) um die Umgebenden Rechteckinformationen zu empfangen. Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich. Die in der **RECT-Struktur** zurückgegebenen Koordinaten werden als Bildschirmkoordinaten ausgedrückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich. Andernfalls **FALSE**.

## <a name="remarks"></a>Hinweise

Das Headersteuerelement muss ein **HDF \_ SPLITBUTTON-Format** aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen zu Headersteuerelementen](header-controls.md)
</dt> </dl>

 

