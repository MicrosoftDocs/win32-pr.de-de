---
title: BCM_SETNOTE (Commctrl.h)
description: Legt den Text der Notiz fest, die einer Befehlslinkschaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das Button \_ SetNote-Makro verwenden.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- BCM_SETNOTE von Windows Steuerelementen
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
ms.openlocfilehash: 82f0f049c1ad8a9837695a1f5d7327883e1dabfb7dd077bd6efce78fa6a0a708
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921550"
---
# <a name="bcm_setnote-message"></a>BCM \_ SETNOTE-Meldung

Legt den Text der Notiz fest, die einer Befehlslinkschaltfläche zugeordnet ist. Sie können diese Nachricht explizit senden oder das [**Button \_ SetNote-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine auf NULL beendete **WCHAR-Zeichenfolge,** die die Notiz enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Ab comctl32 DLL Version 6.01 können Befehlslinkschaltflächen eine Notiz enthalten.

Die **BCM \_ SETNOTE-Nachricht** funktioniert nur mit den [**Schaltflächenstilen BS \_ COMMANDLINK**](button-styles.md) und [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





