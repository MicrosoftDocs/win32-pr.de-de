---
title: HDM_GETITEMDROPDOWNRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck der Trenn Schaltfläche für ein Header Element mit dem Format "HDF \_ SplitButton" ab. Senden Sie diese Nachricht explizit oder mithilfe des Headers \_ getitemdropdownrect-Makros.
ms.assetid: d7188dfb-4ffa-4641-b210-2c2ec480ca13
keywords:
- Windows-Steuerelemente für HDM_GETITEMDROPDOWNRECT Meldung
topic_type:
- apiref
api_name:
- HDM_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86f3df8de5224e79ca4e15ea18409e13972ca5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040640"
---
# <a name="hdm_getitemdropdownrect-message"></a>HDM \_ getitemdropdownrect-Meldung

Ruft das umgebende Rechteck der Trenn Schaltfläche für ein Header Element mit dem Format " **HDF \_ SplitButton**" ab. Senden Sie diese Nachricht explizit oder mithilfe des [**Headers \_ getitemdropdownrect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemdropdownrect) -Makros.

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

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Das Header Element muss den Stil **HDF \_ SplitButton** aufweisen.

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

 

 





