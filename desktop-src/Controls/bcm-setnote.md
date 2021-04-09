---
title: BCM_SETNOTE Meldung (kommstrg. h)
description: Legt den Text des Hinweises fest, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das Schaltflächen- \_ setnote-Makro verwenden.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- Windows-Steuerelemente für BCM_SETNOTE Meldung
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956456"
---
# <a name="bcm_setnote-message"></a>BCM- \_ setnote-Meldung

Legt den Text des Hinweises fest, der einer Befehls Link Schaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das Schaltflächen- [**\_ setnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine NULL terminierte **WCHAR** -Zeichenfolge, die den Hinweis enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Ab ComCtl32 dll, Version 6,01, können Befehls Link Schaltflächen einen Hinweis enthalten.

Die **BCM- \_ setnote** -Nachricht funktioniert nur mit den Schaltflächen Formaten " [**SB \_ CommandLink**](button-styles.md) " und " [**b" \_ defcommandlink**](button-styles.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





