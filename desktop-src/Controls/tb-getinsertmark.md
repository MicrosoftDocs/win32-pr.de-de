---
title: TB_GETINSERTMARK Meldung (Commctrl.h)
description: Ruft die aktuelle Einfügemarke für die Symbolleiste ab.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- TB_GETINSERTMARK Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ee4a51d3110a99013ed26ccb1f2c102e7821873e63dd419b33e92636a1b655
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918750"
---
# <a name="tb_getinsertmark-message"></a>TB \_ GETINSERTMARK-Nachricht

Ruft die aktuelle Einfügemarke für die Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TBINSERTMARK-Struktur,**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) die die Einfügemarke empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **TRUE** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TB \_ SETINSERTMARK**](tb-setinsertmark.md)
</dt> </dl>

 

 





