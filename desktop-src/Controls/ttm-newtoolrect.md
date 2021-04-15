---
title: TTM_NEWTOOLRECT Meldung (kommstrg. h)
description: Legt ein neues Begrenzungs Rechteck für ein Tool fest.
ms.assetid: 81d1b745-310e-482e-8c6e-6e98e1e67b66
keywords:
- Windows-Steuerelemente für TTM_NEWTOOLRECT Meldung
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
ms.openlocfilehash: 75417059b0108877d04c79af25ac98245461ad5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476779"
---
# <a name="ttm_newtoolrect-message"></a>TTM \_ newtoolrect-Meldung

Legt ein neues Begrenzungs Rechteck für ein Tool fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**toolinfo**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) -Struktur. Die **HWND** -und **UID** -Member identifizieren ein Tool, und das **Rect** -Element gibt das neue umgebende Rechteck an. Der **CBSIZE** -Member dieser Struktur muss ausgefüllt werden, bevor diese Nachricht gesendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **TTM \_ Newtoolrectw** (Unicode) und **TTM \_ newtoolrecta** (ANSI)<br/>           |



 

 





