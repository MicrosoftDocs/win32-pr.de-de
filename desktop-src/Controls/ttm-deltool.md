---
title: TTM_DELTOOL Nachricht (Commctrl.h)
description: Entfernt ein Tool aus einem QuickInfo-Steuerelement.
ms.assetid: 433b6f1c-3e9f-4e3a-9834-d447a3f9e6a5
keywords:
- TTM_DELTOOL Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: ea54eefd2b9cc84b3aabe5dd600c5fcc32c7468cae01d1819b5fda7b631aeabd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166383"
---
# <a name="ttm_deltool-message"></a>TTM \_ DELTOOL-Nachricht

Entfernt ein Tool aus einem QuickInfo-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TOOLINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Die **Member hwnd** und **uId** identifizieren das zu entfernende Tool, und der **cbSize-Member** muss die Größe der Struktur angeben. Alle anderen Member werden ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ DELTOOLW** (Unicode) und **TTM \_ DELTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**TTM \_ ADDTOOL**](ttm-addtool.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen zu QuickInfo-Steuerelementen](tooltip-controls.md)
</dt> </dl>

 

 





