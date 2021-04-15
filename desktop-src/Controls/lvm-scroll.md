---
title: LVM_SCROLL Meldung (kommstrg. h)
description: Scrollt den Inhalt eines Listenansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ scrollmakros senden.
ms.assetid: 4bf6b74e-8fea-48ca-a151-8fd649fc50f8
keywords:
- Windows-Steuerelemente für LVM_SCROLL Meldung
topic_type:
- apiref
api_name:
- LVM_SCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05c3ed991cfc933a4436baf332b49c67a907b11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477559"
---
# <a name="lvm_scroll-message"></a>LVM- \_ scrollnachricht

Scrollt den Inhalt eines Listenansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des [**ListView- \_ scrollmakros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_scroll) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Wert vom Typ " **int** ", der den horizontalen Bildlauf in Pixel relativ zur aktuellen Position des Listen Ansichts Inhalts angibt. Wenn sich das Listenansicht-Steuerelement in der Listenansicht befindet, wird dieser Wert auf die nächste Anzahl von Pixeln aufgerundet, die eine ganze Spalte bilden.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Wert vom Typ " **int** ", der den vertikalen Bildlauf in Pixel relativ zur aktuellen Position des Listen Ansichts Inhalts angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Wenn sich das Listenansicht-Steuerelement in der Berichtsansicht befindet, kann das Steuerelement nur vertikal in Zeilen Inkrementen gescrollt werden. Daher wird der *LPARAM* -Parameter auf die nächste Anzahl von Pixeln gerundet, die ein ganzes Zeilen Inkrement bilden. Wenn z. b. die Höhe einer Linie 16 Pixel und 8 für *LPARAM* überschritten wird, wird die Liste um 16 Pixel (1 Zeile) gescrollt. Wenn für *LPARAM* der Wert 7 festgelegt wird, wird für die Liste der Bildlauf mit 0 Pixel (0 Zeilen) durchgeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





