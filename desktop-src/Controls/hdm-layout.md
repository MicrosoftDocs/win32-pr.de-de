---
title: HDM_LAYOUT (Commctrl.h)
description: Ruft Informationen ab, die zum Festlegen der Größe und Position des Header-Steuerelements innerhalb des Zielrechtecks des übergeordneten Fensters verwendet werden. Sie können diese Nachricht explizit senden oder das Makro \_ Headerlayout verwenden.
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4194ad5aa1847aa977bac1269a7ab88d36a571824387e07264713726135f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435930"
---
# <a name="hdm_layout-message"></a>\_HDM-LAYOUTmeldung

Ruft Informationen ab, die zum Festlegen der Größe und Position des Header-Steuerelements innerhalb des Zielrechtecks des übergeordneten Fensters verwendet werden. Sie können diese Nachricht explizit senden oder das Makro [**\_ Headerlayout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**HDLAYOUT-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) Das **PRC-Element** gibt die Koordinaten eines Rechtecks an, und das **pwpos-Element** empfängt die Größe und Position für das Header-Steuerelement innerhalb des Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Der **pwpos-Member** der *lParam-Struktur* empfängt Größen- und Positionswerte, die für die Positionierung des Steuerelements am oberen Ende des angegebenen Rechtecks geeignet sind. Der Höhenwert ist die Summe der Höhe der horizontalen Rahmen des Steuerelements und der durchschnittlichen Höhe der Zeichen in der Schriftart, die derzeit im Gerätekontext des Steuerelements ausgewählt ist.

Um **HDM \_ LAYOUT** zum Festlegen der Anfangsgröße und -position eines Header-Steuerelements zu verwenden, legen Sie den anfänglichen Sichtbarkeitszustand des Steuerelements so fest, dass es ausgeblendet wird. Verwenden Sie nach dem Senden von **HDM \_ LAYOUT** zum Abrufen der Werte für Größe und Position die [**Funktion SetWindowPos,**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) um die neue Größe, Position und den Sichtbarkeitszustand zu festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

