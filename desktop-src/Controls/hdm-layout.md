---
title: HDM_LAYOUT Meldung (kommstrg. h)
description: Ruft Informationen ab, die zum Festlegen der Größe und Position des Header Steuer Elements innerhalb des Ziel Rechtecks des übergeordneten Fensters verwendet werden. Sie können diese Nachricht explizit senden oder das Header \_ Layout-Makro verwenden.
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- Windows-Steuerelemente für HDM_LAYOUT Meldung
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
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040638"
---
# <a name="hdm_layout-message"></a>HDM- \_ layoutmeldung

Ruft Informationen ab, die zum Festlegen der Größe und Position des Header Steuer Elements innerhalb des Ziel Rechtecks des übergeordneten Fensters verwendet werden. Sie können diese Nachricht explizit senden oder das [**Header \_ Layout**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**hdlayout**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) -Struktur. Der **PRC** -Member gibt die Koordinaten eines Rechtecks an, und das **pwpos** -Element empfängt die Größe und Position des Header Steuer Elements innerhalb des Rechtecks.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Der **pwpos** -Member der *LPARAM* -Struktur erhält Größen-und Positionswerte, die für die Positionierung des Steuer Elements am oberen Rand des angegebenen Rechtecks geeignet sind. Der Height-Wert ist die Summe der Höhe der horizontalen Rahmen des Steuer Elements und die durchschnittliche Höhe der Zeichen in der Schriftart, die derzeit im Gerätekontext des Steuer Elements ausgewählt ist.

Um das **HDM- \_ Layout** zum Festlegen der Anfangs Größe und Position eines Header Steuer Elements zu verwenden, legen Sie den ursprünglichen Sichtbarkeits Zustand des-Steuer Elements so fest, dass es ausgeblendet ist. Nach dem Senden des **HDM- \_ Layouts** zum Abrufen der Größen-und Positionswerte verwenden Sie die [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion, um die neue Größe, Position und den Sichtbarkeits Zustand festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

