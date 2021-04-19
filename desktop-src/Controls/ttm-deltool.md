---
title: TTM_DELTOOL Meldung (kommstrg. h)
description: Entfernt ein Tool aus einem QuickInfo-Steuerelement.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- Windows-Steuerelemente für TTM_DELTOOL Meldung
topic_type:
- apiref
api_name:
- TTM_DELTOOL
- TTM_DELTOOLA
- TTM_DELTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943259c5496757c0f15ca4127d0a5e6a4237fbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341388"
---
# <a name="ttm_deltool-message"></a>TTM \_ Delta Tool-Meldung

Entfernt ein Tool aus einem QuickInfo-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur. Die **HWND** -und **UID** -Member identifizieren das zu entfernenden Tool, und das **CBSIZE** -Element muss die Größe der Struktur angeben. Alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Delta toolw** (Unicode) und **TTM \_ Delta** (ANSI)<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**TTM \_ AddTool**](ttm-addtool.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Info-Steuerelemente](tooltip-controls.md)
</dt> </dl>

 

 





