---
title: TTM_NEWTOOLRECT (Commctrl.h)
description: Legt ein neues umgebundenes Rechteck für ein Tool fest.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- TTM_NEWTOOLRECT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TTM_NEWTOOLRECT
- TTM_NEWTOOLRECTA
- TTM_NEWTOOLRECTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13889b0e9c0d80392b88130c33e5e9723ceb776a60a6b941d205d514d96ca22f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750980"
---
# <a name="ttm_newtoolrect-message"></a>TTM \_ NEWTOOLRECT-Meldung

Legt ein neues umgebundenes Rechteck für ein Tool fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**TOOLINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Die **Elemente hwnd** und **uId** identifizieren ein Tool, und das **Rect-Element** gibt das neue umschlossene Rechteck an. Der **cbSize-Member** dieser -Struktur muss vor dem Senden dieser Nachricht ausgefüllt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ NEWTOOLRECTW** (Unicode) und **TTM \_ NEWTOOLRECTA** (ANSI)<br/>           |



 

 





