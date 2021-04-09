---
title: RB_SIZETORECT Meldung (kommstrg. h)
description: Versucht, das beste Layout der Bänder für das angegebene Rechteck zu finden.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- Windows-Steuerelemente für RB_SIZETORECT Meldung
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106251"
---
# <a name="rb_sizetorect-message"></a>RB \_ sizetorect-Nachricht

Versucht, das beste Layout der Bänder für das angegebene Rechteck zu finden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck angibt, mit dem das Grund leisten Steuerelement vergrößert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert ungleich 0 (null) zurück, wenn eine Layoutänderung aufgetreten ist, andernfalls

## <a name="remarks"></a>Bemerkungen

Die Grund leisten Bänder werden nach Bedarf angeordnet und umschließt, damit Sie an das Rechteck angepasst werden. Für Bänder mit dem RBBS- \_ variableheight-Stil wird die Größe so gleichmäßig wie möglich angepasst, damit Sie dem Rechteck entspricht. Abhängig vom neuen Layout kann die Höhe einer horizontalen Info Leiste oder die Breite einer vertikalen Grund Leiste geändert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

