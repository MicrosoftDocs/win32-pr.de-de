---
title: CBEM_INSERTITEM Meldung (Commctrl.h)
description: Fügt ein neues Element in ein ComboBoxEx-Steuerelement ein.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4d9627efef4796554dfdbe1d7263747cc6b1c32b2cc00d5619a7cb7953024cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699306"
---
# <a name="cbem_insertitem-message"></a>CBEM \_ INSERTITEM-Nachricht

Fügt ein neues Element in ein ComboBoxEx-Steuerelement ein.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**COMBOBOXEXITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) die Informationen über das einzufügende Element enthält. Wenn die Nachricht gesendet wird, muss das **iItem-Element** so festgelegt werden, dass er den nullbasierten Index angibt, an dem das Element eingefügt werden soll. Um ein Element am Ende der Liste einzufügen, legen Sie das **iItem-Element** auf -1 fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index zurück, an dem das neue Element bei Erfolg eingefügt wurde, andernfalls -1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **CBEM \_ INSERTITEMW** (Unicode) und **CBEM \_ INSERTITEMA** (ANSI)<br/>           |



 

 





