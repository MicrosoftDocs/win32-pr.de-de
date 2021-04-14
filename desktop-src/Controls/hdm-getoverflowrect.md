---
title: HDM_GETOVERFLOWRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck der Überlauf Schaltfläche ab, wenn der HDS \_ -Überlauf Stil für das Header Steuerelement festgelegt ist und die Überlauf Schaltfläche sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des GetOverflowRect-Makros des Headers \_ .
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- Windows-Steuerelemente für HDM_GETOVERFLOWRECT Meldung
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
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518119"
---
# <a name="hdm_getoverflowrect-message"></a>HDM \_ GETOVERFLOWRECT Meldung

Ruft das umgebende Rechteck der Überlauf Schaltfläche ab, wenn der [**HDS- \_ Überlauf**](header-control-styles.md) Stil für das Header Steuerelement festgelegt ist und die Überlauf Schaltfläche sichtbar ist. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ GetOverflowRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) -Makros des Headers.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet. Muss Null sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, um die umschließenden Rechteck Informationen zu erhalten. Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich. Die in der **Rect** -Struktur zurückgegebenen Koordinaten werden als Bildschirm Koordinaten ausgedrückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Das Header Steuerelement muss den Stil **HDF \_ SplitButton** aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Informationen über Header Steuerelemente](header-controls.md)
</dt> </dl>

 

