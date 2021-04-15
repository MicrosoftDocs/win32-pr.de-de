---
title: HDM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für ein angegebenes Element in einem Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das-Header \_ GetItemRect-Makro verwenden.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- Windows-Steuerelemente für HDM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477583"
---
# <a name="hdm_getitemrect-message"></a>HDM- \_ GetItemRect-Nachricht

Ruft das umgebende Rechteck für ein angegebenes Element in einem Header Steuerelement ab. Sie können diese Nachricht explizit senden oder das- [**Header \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der null basierte Index des Header Steuerelement Elements, für das das umgebende Rechteck abgerufen werden soll.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/windows/win32/api/windef/ns-windef-rect) -Struktur, die die umschließenden Rechteck Informationen empfängt. Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich. Die in der Rect-Struktur zurückgegebenen Koordinaten werden relativ zum übergeordneten Header Steuerelement ausgedrückt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





