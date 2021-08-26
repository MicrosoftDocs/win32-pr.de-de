---
title: LVM_SETCOLUMNWIDTH Meldung (Commctrl.h)
description: Ändert die Breite einer Spalte im Berichtsansichtsmodus oder die Breite aller Spalten im Listenansichtsmodus. Sie können diese Nachricht explizit senden oder das \_ ListView-Makro SetColumnWidth verwenden.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH Windows-Steuerelementen
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
ms.openlocfilehash: 7a127706d6a47444ee59f1434478aadb5170f9ac7a919dca6fd6151de33486d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077290"
---
# <a name="lvm_setcolumnwidth-message"></a>LVM \_ SETCOLUMNWIDTH-Nachricht

Ändert die Breite einer Spalte im Berichtsansichtsmodus oder die Breite aller Spalten im Listenansichtsmodus. Sie können diese Nachricht explizit senden oder das [**\_ ListView-Makro SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index einer gültigen Spalte. Für den Listenansichtsmodus muss dieser Parameter auf 0 (null) festgelegt werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue Breite der Spalte in Pixel. Für den Berichtsansichtsmodus werden die folgenden speziellen Werte unterstützt:



| Wert                                                                                                                                                                                           | Bedeutung                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**LVSCW \_ AUTOIZE**</dt> </dl>                                | Passt die Größe der Spalte automatisch an.<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AUTOIZE \_ USEHEADER**</dt> </dl> | Passt die Spalte automatisch an den Headertext an. Wenn Sie diesen Wert mit der letzten Spalte verwenden, wird die Breite so festgelegt, dass die verbleibende Breite des Listenansichtssteuerelements ausgefüllt wird.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="remarks"></a>Hinweise

Angenommen, Sie verfügen über ein 2-Spalten-Listenansicht-Steuerelement mit einer Breite von 500 Pixeln. Wenn die Breite der Spalte 0 auf 200 Pixel festgelegt ist und Sie diese Nachricht mit *wParam* = 1 und *lParam* = LVSCW \_ AUTOSIZE \_ USEHEADER senden, ist die zweite (und letzte) Spalte 300 Pixel breit.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





