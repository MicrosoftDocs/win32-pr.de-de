---
title: LVM_APPROXIMATEVIEWRECT (Commctrl.h)
description: Berechnet die ungefähre Breite und Höhe, die zum Anzeigen einer bestimmten Anzahl von Elementen erforderlich sind. Sie können diese Nachricht explizit senden oder das ListView \_ ApproximateViewRect-Makro verwenden.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT von Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fcbb5476f28debd28116a52123bd01b8030c8b0a0c9c52e6598c864caed021
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047060"
---
# <a name="lvm_approximateviewrect-message"></a>LVM \_ APPROXIMATEVIEWRECT-Nachricht

Berechnet die ungefähre Breite und Höhe, die zum Anzeigen einer bestimmten Anzahl von Elementen erforderlich sind. Sie können diese Nachricht explizit senden oder das [**ListView \_ ApproximateViewRect-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Elemente, die im -Steuerelement angezeigt werden sollen. Wenn dieser Parameter auf -1 festgelegt ist, verwendet die Nachricht die Gesamtzahl der Elemente im -Steuerelement.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LOWORD ist**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die vorgeschlagene x-Dimension des Steuerelements in Pixel. Dieser Parameter kann auf -1 festgelegt werden, damit die Nachricht den aktuellen Breitenwert verwenden kann.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist die vorgeschlagene y-Dimension des Steuerelements in Pixel. Dieser Parameter kann auf -1 festgelegt werden, damit die Nachricht den aktuellen Höhenwert verwenden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der die ungefähre Breite (im [**LOWORD)**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))und die Höhe (im [**HIWORD)**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))enthält, die zum Anzeigen der Elemente in Pixel erforderlich sind.

## <a name="remarks"></a>Hinweise

Das Festlegen der Größe des Listenansicht-Steuerelements basierend auf den von dieser Meldung bereitgestellten Dimensionen kann das Neuzeichneten optimieren und das Flackern reduzieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

