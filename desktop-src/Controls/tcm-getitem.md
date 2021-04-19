---
title: TCM_GETITEM Meldung (kommstrg. h)
description: Ruft Informationen zu einer Registerkarte in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ GetItem-Makros senden.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- Windows-Steuerelemente für TCM_GETITEM Meldung
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
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343469"
---
# <a name="tcm_getitem-message"></a>TCM \_ GetItem-Nachricht

Ruft Informationen zu einer Registerkarte in einem Registerkarten-Steuerelement ab. Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Index der Registerkarte.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur, die die Informationen angibt, die abgerufen und Informationen über die Registerkarte empfangen werden. Wenn die Nachricht gesendet wird, gibt der **Mask** -Member an, welche Attribute zurückgegeben werden sollen. Wenn das **Mask** -Element den tcif- \_ Textwert angibt, muss der **pszText** -Member die Adresse des Puffers enthalten, der den Element Text empfängt, und der **cchtextmax** -Member muss die Größe des Puffers angeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Wenn das tcif- \_ textflag im **Mask** -Member der [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) -Struktur festgelegt ist, kann das Steuerelement den **pszText** -Member der Struktur so ändern, dass er auf den neuen Text verweist, anstatt den Puffer mit dem angeforderten Text zu füllen. Das-Steuerelement kann den **pszText** -Member auf **null** festlegen, um anzugeben, dass dem Element kein Text zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TCM \_ Getitemw** (Unicode) und **TCM \_ getitema** (ANSI)<br/>                   |



 

 





