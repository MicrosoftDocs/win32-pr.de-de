---
title: LVM_SETCOLUMNWIDTH Meldung (kommstrg. h)
description: Ändert die Breite einer Spalte im Berichts Ansichtsmodus oder die Breite aller Spalten im Listen Ansichtsmodus. Sie können diese Nachricht explizit senden oder das ListView \_ setcolumnwidth-Makro verwenden.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- Windows-Steuerelemente für LVM_SETCOLUMNWIDTH Meldung
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102891"
---
# <a name="lvm_setcolumnwidth-message"></a>LVM- \_ setcolumnwidth-Nachricht

Ändert die Breite einer Spalte im Berichts Ansichtsmodus oder die Breite aller Spalten im Listen Ansichtsmodus. Sie können diese Nachricht explizit senden oder das [**ListView \_ setcolumnwidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index einer gültigen Spalte. Für den Listen Ansichtsmodus muss dieser Parameter auf 0 (null) festgelegt werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Die neue Breite der Spalte in Pixel. Für den Berichts Ansichtsmodus werden die folgenden speziellen Werte unterstützt:



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**Automatische Größe des lvscw \_**</dt> </dl>                                | Passt die Größe der Spalte automatisch an.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**"lvscw \_ AutoSize"- \_ useheader**</dt> </dl> | Passt die Größe der Spalte automatisch an den Header Text an. Wenn Sie diesen Wert mit der letzten Spalte verwenden, wird seine Breite so festgelegt, dass die verbleibende Breite des Listenansicht-Steuer Elements ausgefüllt wird.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Angenommen, Sie verfügen über ein zweispaltige Listenansicht-Steuerelement mit einer Breite von 500 Pixeln. Wenn die Breite der Spalte NULL auf 200 Pixel festgelegt ist und Sie diese Nachricht mit *wParam* = 1 und *LPARAM* = lvscw \_ AutoSize \_ useheader senden, wird die zweite (und letzte) Spalte 300 Pixel breit.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





