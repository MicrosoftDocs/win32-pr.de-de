---
title: LVM_GETITEMRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für den gesamten oder einen Teil eines Elements in der aktuellen Ansicht ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemRect-Makros senden.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- Windows-Steuerelemente für LVM_GETITEMRECT Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040890"
---
# <a name="lvm_getitemrect-message"></a>LVM- \_ GetItemRect-Nachricht

Ruft das umgebende Rechteck für den gesamten oder einen Teil eines Elements in der aktuellen Ansicht ab. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Der Index des Listen Ansichts Elements.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das umschließende Rechteck empfängt. Wenn die Nachricht gesendet wird, wird der **linke** Member dieser Struktur verwendet, um den Teil des Listen Ansichts Elements anzugeben, aus dem das umgebende Rechteck abgerufen werden soll. Für sie muss einer der folgenden Werte festgelegt werden:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**lvir- \_ Begrenzungen**</dt> </dl>                   | Gibt das umgebende Rechteck des gesamten Elements zurück, einschließlich des Symbols und der Bezeichnung.<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**lvir- \_ Symbol**</dt> </dl>                         | Gibt das umgebende Rechteck des Symbols oder des kleinen Symbols zurück.<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**lvir- \_ Bezeichnung**</dt> </dl>                      | Gibt das umgebende Rechteck des Element Texts zurück.<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**lvir- \_ selectbounds**</dt> </dl> | Gibt die Gesamtmenge des lvir \_ -Symbols und der lvir- \_ Beschriftungs Rechtecke zurück, schließt jedoch Spalten in der Berichtsansicht aus.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

