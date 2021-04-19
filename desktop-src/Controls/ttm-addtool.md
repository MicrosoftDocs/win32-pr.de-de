---
title: TTM_ADDTOOL Meldung (kommstrg. h)
description: Registriert ein Tool mit einem QuickInfo-Steuerelement.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- Windows-Steuerelemente für TTM_ADDTOOL Meldung
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29dad3e297f8c3430f18286afa9a998eaf578a26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341800"
---
# <a name="ttm_addtool-message"></a>TTM \_ AddTool-Meldung

Registriert ein Tool mit einem QuickInfo-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur, die Informationen enthält, die das QuickInfo-Steuerelement zum Anzeigen von Text für das Tool benötigt. Der **CBSIZE** -Member dieser Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Addtoolw** (Unicode) und **TTM \_ AddIn** (ANSI)<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TTM \_ Delta Tool**](ttm-deltool.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Info-Steuerelemente](tooltip-controls.md)
</dt> </dl>

 

 





