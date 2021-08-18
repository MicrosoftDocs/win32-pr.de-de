---
title: TB_GETITEMDROPDOWNRECT (Commctrl.h)
description: Ruft das umgebundene Rechteck des Dropdownfensters für ein Symbolleistenelement mit dem Stil BTNS \_ DROPDOWN ab.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd2dfc8a48ff735bfb8bcc99bc0baf36555eee9d995c3f453a95ea2910948a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918700"
---
# <a name="tb_getitemdropdownrect-message"></a>TB \_ GETITEMDROPDOWNRECT-Nachricht

Ruft das umgebundene Rechteck des Dropdownfensters für ein Symbolleistenelement mit dem Stil [**BTNS \_ DROPDOWN ab.**](toolbar-control-and-button-styles.md)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Der nullbasierte Index des Symbolleisten-Steuerelementelements, für das das umgebundene Rechteck abgerufen werden soll.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Ein Zeiger auf eine <a href="/previous-versions//dd162897(v=vs.85)">**RECT-Struktur,**</a> um die Informationen zum umgebundenen Rechteck zu empfangen. Der Absender der Nachricht ist für die Zuordnung dieser Struktur verantwortlich. Die in der **RECT-Struktur zurückgegebenen Koordinaten** werden als Clientkoordinaten ausgedrückt.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt immer einen Wert ungleich 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Das Element muss das [**BTNS-DROPDOWN-Format \_**](toolbar-control-and-button-styles.md) haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

