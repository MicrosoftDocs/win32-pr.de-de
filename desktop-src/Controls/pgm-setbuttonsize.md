---
title: PGM_SETBUTTONSIZE Meldung (kommstrg. h)
description: Legt die aktuelle Schaltflächen Größe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das Pager- \_ setbuttonsize-Makro verwenden.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- Windows-Steuerelemente für PGM_SETBUTTONSIZE Meldung
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517645"
---
# <a name="pgm_setbuttonsize-message"></a>PGM- \_ setbuttonsize-Meldung

Legt die aktuelle Schaltflächen Größe für das Pager-Steuerelement fest. Sie können diese Nachricht explizit senden oder das [**Pager- \_ setbuttonsize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert vom Typ **int** , der die neue Schaltflächen Größe in Pixel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **int** -Wert zurück, der die vorherige Schaltflächen Größe in Pixel enthält.

## <a name="remarks"></a>Bemerkungen

Wenn das Pager-Steuerelement den [**PGS- \_ Horz**](pager-control-styles.md) -Stil hat, bestimmt die Schaltflächen Größe die Breite der Pager-Schaltflächen. Wenn das Pager-Steuerelement den [**PGS \_**](pager-control-styles.md) -Stil hat, bestimmt die Schaltflächen Größe die Höhe der Pager-Schaltflächen. Standardmäßig legt das Pager-Steuerelement seine Schaltflächen Größe auf drei Zehntel der Breite der Bild Lauf Leiste fest.

Es gibt eine Mindestgröße für die Pager-Schaltfläche, derzeit 12 Pixel. Dies kann sich jedoch ändern, sodass Sie nicht von diesem Wert abhängig sein sollten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PGM \_ getbuttonsize**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





