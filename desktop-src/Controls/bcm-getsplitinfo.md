---
title: BCM_GETSPLITINFO (Commctrl.h)
description: Ruft Informationen für ein Steuerelement für geteilte Schaltflächen ab. Senden Sie diese Nachricht explizit oder mithilfe des \_ Button GetSplitInfo-Makros.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- BCM_GETSPLITINFO meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ee0771c8999c6a805931a93ed28c245082d18e538856fde42b69622ee73f9a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921640"
---
# <a name="bcm_getsplitinfo-message"></a>BCM \_ GETSPLITINFO-Nachricht

Ruft Informationen für ein Steuerelement für geteilte Schaltflächen ab. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ Button GetSplitInfo-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**BUTTON \_ SPLITINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) um Informationen über die Schaltfläche zu empfangen. Der Aufrufer ist für die Zuweisung des Arbeitsspeichers für die -Struktur verantwortlich. Legen  Sie den Masken-Member dieser -Struktur fest, um zu bestimmen, welche Informationen empfangen werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Meldung nur mit den [**Schaltflächenstilen BS \_ SPLITBUTTON**](button-styles.md) und [**BS \_ DEFSPLITBUTTON.**](button-styles.md)

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

 

 





