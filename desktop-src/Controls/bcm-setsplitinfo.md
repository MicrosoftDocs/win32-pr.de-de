---
title: BCM_SETSPLITINFO Meldung (kommstrg. h)
description: Legt Informationen für ein unterteilte Schaltflächen Steuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe der Schaltfläche \_ setsplitinfo-Makro.
ms.assetid: 609b8972-9616-4850-a72c-2f87ce19f563
keywords:
- Windows-Steuerelemente für BCM_SETSPLITINFO Meldung
topic_type:
- apiref
api_name:
- BCM_SETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac40f2d1ef016ee76ab21ccf2dc4733d0ff427f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340794"
---
# <a name="bcm_setsplitinfo-message"></a>BCM- \_ setsplitinfo-Meldung

Legt Informationen für ein unterteilte Schaltflächen Steuerelement fest. Senden Sie diese Nachricht explizit oder mithilfe der [**Schaltfläche \_ setsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) -Makro.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*LPARAM* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**\_ splitinfo**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) -Struktur der Schaltfläche, die Informationen über die unterteilte Schaltfläche enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung nur mit den Schaltflächen Stilen [**\_ SplitButton**](button-styles.md) und [**SB \_ defsplitbutton**](button-styles.md) .

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

 

 





