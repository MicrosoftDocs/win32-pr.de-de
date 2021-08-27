---
title: TB_INSERTMARKHITTEST Meldung (Commctrl.h)
description: Ruft die Einfügemarkierungsinformationen für einen Punkt in einer Symbolleiste ab.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc231b915d6d71cc22ee3cd98b1c6dd602451cc3c70d2153ba1bee8a0d55657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061360"
---
# <a name="tb_insertmarkhittest-message"></a>TB \_ INSERTMARKHITTEST-Nachricht

Ruft die Einfügemarkierungsinformationen für einen Punkt in einer Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine [**POINT-Struktur,**](/previous-versions//dd162805(v=vs.85)) die die Treffertestkoordinaten relativ zum Clientbereich der Symbolleiste enthält.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TBINSERTMARK-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) die die Einfügemarkierungsinformationen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn der Punkt eine Einfügemarke ist, andernfalls 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

