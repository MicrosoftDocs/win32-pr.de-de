---
title: TCM_GETITEM Meldung (Commctrl.h)
description: Ruft Informationen zu einer Registerkarte in einem Registerkartensteuerelement ab. Sie können diese Nachricht explizit oder mithilfe des \_ GetItem-Makros TabCtrl senden.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- TCM_GETITEM Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5403bb85e1b2747d1ab6081d33c25ec20a3b2099fc83b2b15e66b014f558584
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876580"
---
# <a name="tcm_getitem-message"></a>TCM \_ GETITEM-Nachricht

Ruft Informationen zu einer Registerkarte in einem Registerkartensteuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**\_ GetItem-Makros TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der Registerkarte.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TCITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-tcitema) die die abzurufenden Informationen angibt und Informationen über die Registerkarte empfängt. Wenn die Nachricht gesendet wird, gibt der **Maskenmember** an, welche Attribute zurückgegeben werden sollen. Wenn der **Maskenmember** den TCIF \_ TEXT-Wert angibt, muss das **pszText-Element** die Adresse des Puffers enthalten, der den Elementtext empfängt, und der **cchTextMax-Member** muss die Größe des Puffers angeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Wenn das TCIF \_ TEXT-Flag im **Maskenmember** der [**TCITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-tcitema) festgelegt ist, kann das Steuerelement den **pszText-Member** der -Struktur so ändern, dass er auf den neuen Text zeigt, anstatt den Puffer mit dem angeforderten Text aufzufüllen. Das Steuerelement kann den **pszText-Member** auf **NULL** festlegen, um anzugeben, dass dem Element kein Text zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TCM \_ GETITEMW** (Unicode) und **TCM \_ GETITEMA** (ANSI)<br/>                   |



 

 





