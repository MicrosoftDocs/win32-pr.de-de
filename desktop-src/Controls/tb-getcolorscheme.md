---
title: TB_GETCOLORSCHEME Meldung (kommstrg. h)
description: Ruft die Farbschema Informationen aus dem Symbolleisten-Steuerelement ab.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- Windows-Steuerelemente für TB_GETCOLORSCHEME Meldung
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477106"
---
# <a name="tb_getcolorscheme-message"></a>TB \_ getcolorscheme-Meldung

Ruft die Farbschema Informationen aus dem Symbolleisten-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) -Struktur, die die Farbschema Informationen empfängt. Sie müssen den **CBSIZE** -Member dieser Struktur auf **sizeof**(ColorScheme) festlegen, bevor Sie diese Nachricht senden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TB \_ SetColorScheme**](tb-setcolorscheme.md)
</dt> </dl>

 

 





