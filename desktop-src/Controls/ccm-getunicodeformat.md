---
title: CCM_GETUNICODEFORMAT Meldung (Commctrl.h)
description: Ruft das Unicode-Zeichenformatflag für das -Steuerelement ab.
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- CCM_GETUNICODEFORMAT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa115ba341478990b46600bc76ee02e4ecf750d5a7ccde9f1110aa8856d30fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438280"
---
# <a name="ccm_getunicodeformat-message"></a>CCM \_ GETUNICODEFORMAT-Nachricht

Ruft das Unicode-Zeichenformatflag für das -Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Unicode-Formatflag für das Steuerelement zurück. Wenn dieser Wert ungleich 0 (null) ist, verwendet das Steuerelement Unicode-Zeichen. Wenn dieser Wert 0 (null) ist, verwendet das Steuerelement ANSI-Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md)
</dt> </dl>

 

 





