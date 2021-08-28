---
title: LVM_GETITEMINDEXRECT Nachricht (Commctrl.h)
description: Ruft das umgrenzende Rechteck für ein gesamtes oder einen Teil eines Unterelements in der aktuellen Ansicht eines Listenansichtssteuerelements ab. Senden Sie diese Nachricht explizit oder mithilfe des \_ ListView-Makros GetItemIndexRect.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91aa3e6d0420bfddb974d13f210c84241cefc5d79f0ee5a82920bdc2961879dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770370"
---
# <a name="lvm_getitemindexrect-message"></a>LVM \_ GETITEMINDEXRECT-Nachricht

Ruft das umgrenzende Rechteck für ein gesamtes oder einen Teil eines Unterelements in der aktuellen Ansicht eines Listenansichtssteuerelements ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemIndexRect-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**LVITEMINDEX-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) für das übergeordnete Element des Unterelements. Der aufrufende Prozess ist dafür verantwortlich, diese Struktur zuzuordnen und ihre Member festzulegen. *wParam* darf nicht **NULL** sein.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**RECT-Struktur,**](/previous-versions//dd162897(v=vs.85)) um die Koordinaten zu empfangen. Der aufrufende Prozess ist für die Zuordnung dieser Struktur verantwortlich. *lParam* darf nicht **NULL** sein. Legen Sie den **obersten** Member auf den Index des Unteritems fest. Legen Sie den **linken** Member auf einen der folgenden Werte fest, der den Teil des Unteritems angibt, für den das umgebende Rechteck abgerufen werden soll.



| Wert                                                                                                                                                   | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**\_LVIR-BEGRENZUNGEN**</dt> </dl> | Gibt das umgrenzende Rechteck des gesamten Unterzeichens zurück, einschließlich des Symbols und der Bezeichnung.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**\_LVIR-SYMBOL**</dt> </dl>       | Gibt das umgrenzende Rechteck des Symbols oder des kleinen Symbols des Unteritems zurück.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**\_LVIR-BEZEICHNUNG**</dt> </dl>    | Gibt das umgrenzende Rechteck des Unteritemtexts zurück.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn erfolgreich, **andernfalls FALSE.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

