---
title: RB_SETBARINFO (Commctrl.h)
description: Legt die Merkmale eines Rebar-Steuerelements fest.
ms.assetid: e4413d46-574f-4ccd-b5fd-3ba6c1e3924b
keywords:
- RB_SETBARINFO meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- RB_SETBARINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4297d73a8bca6abac1a4b99abc4a91147ad237548a67e325a9efb2f1a1f1c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696610"
---
# <a name="rb_setbarinfo-message"></a>RB \_ SETBARINFO-Meldung

Legt die Merkmale eines Rebar-Steuerelements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**REBARINFO-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) die die zu setzenden Informationen enthält. Sie müssen den **cbSize-Member** dieser -Struktur auf **sizeof**(REBARINFO) festlegen, bevor Sie diese Nachricht senden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





