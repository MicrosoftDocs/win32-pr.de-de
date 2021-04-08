---
title: LVM_APPROXIMATEVIEWRECT Meldung (kommstrg. h)
description: Berechnet die ungefähre Breite und Höhe, die erforderlich sind, um eine bestimmte Anzahl von Elementen anzuzeigen. Sie können diese Nachricht explizit senden oder das ListView- \_ Suffix "näherateviewrect" verwenden.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- Windows-Steuerelemente für LVM_APPROXIMATEVIEWRECT Meldung
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
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949429"
---
# <a name="lvm_approximateviewrect-message"></a>LVM- \_ ungefähre näherungsviewrect-Nachricht

Berechnet die ungefähre Breite und Höhe, die erforderlich sind, um eine bestimmte Anzahl von Elementen anzuzeigen. Sie können diese Nachricht explizit senden oder das [**ListView- \_ Suffix "näherateviewrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) " verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anzahl der Elemente, die im Steuerelement angezeigt werden sollen. Wenn dieser Parameter auf-1 festgelegt ist, wird die Gesamtzahl der Elemente im-Steuerelement in der Nachricht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist die vorgeschlagene x-Dimension des-Steuer Elements in Pixel. Dieser Parameter kann auf-1 festgelegt werden, damit die Nachricht den aktuellen width-Wert verwenden kann.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist die vorgeschlagene y-Dimension des-Steuer Elements in Pixel. Dieser Parameter kann auf-1 festgelegt werden, damit die Nachricht den aktuellen Height-Wert verwenden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der die ungefähre Breite (im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) und die Höhe (im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) für die Anzeige der Elemente in Pixel enthält.

## <a name="remarks"></a>Bemerkungen

Das Festlegen der Größe des Listenansicht-Steuer Elements auf der Grundlage der Dimensionen, die von dieser Nachricht bereitgestellt werden, kann das Neuzeichnen und reduzieren der Flimmern optimieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

