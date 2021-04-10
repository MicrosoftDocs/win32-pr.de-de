---
title: TB_GETINSERTMARK Meldung (kommstrg. h)
description: Ruft die aktuelle Einfügemarke für die Symbolleiste ab.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- Windows-Steuerelemente für TB_GETINSERTMARK Meldung
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
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040232"
---
# <a name="tb_getinsertmark-message"></a>TB \_ getinsertmark-Nachricht

Ruft die aktuelle Einfügemarke für die Symbolleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**tbinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) -Struktur, die die Einfügemarke empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB- \_ Einfügemarke**](tb-setinsertmark.md)
</dt> </dl>

 

 





