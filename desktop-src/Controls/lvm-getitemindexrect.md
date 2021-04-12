---
title: LVM_GETITEMINDEXRECT Meldung (kommstrg. h)
description: Ruft das umgebende Rechteck für den gesamten oder einen Teil eines unter Elements in der aktuellen Ansicht eines Listenansicht-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des ListView \_ getitemindexrect-Makros.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- Windows-Steuerelemente für LVM_GETITEMINDEXRECT Meldung
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
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478522"
---
# <a name="lvm_getitemindexrect-message"></a>LVM- \_ getitemindexrect-Nachricht

Ruft das umgebende Rechteck für den gesamten oder einen Teil eines unter Elements in der aktuellen Ansicht eines Listenansicht-Steuer Elements ab. Senden Sie diese Nachricht explizit oder mithilfe des [**ListView \_ getitemindexrect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) -Makros.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**lvitemindex**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) -Struktur für das übergeordnete Element des unter Elements. Der Aufrufprozess ist dafür verantwortlich, diese Struktur zuzuordnen und deren Member festzulegen. *wParam* darf nicht **null** sein.

</dd> <dt>

*LPARAM* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Koordinaten empfängt. Der Aufrufprozess ist für die Zuordnung dieser Struktur verantwortlich. *LPARAM* darf nicht **null** sein. Legen Sie den **obersten** Member auf den Index des unter Elements fest. Legen Sie den **linken** Member auf einen der folgenden Werte fest, um den Teil des unter Elements anzugeben, für das das umgebende Rechteck abgerufen werden soll.



| Wert                                                                                                                                                   | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**lvir- \_ Begrenzungen**</dt> </dl> | Gibt das umgebende Rechteck des gesamten unter Elements zurück, einschließlich des Symbols und der Bezeichnung.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**lvir- \_ Symbol**</dt> </dl>       | Gibt das umgebende Rechteck des Symbols oder des kleinen Symbols des unter Elements zurück.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**lvir- \_ Bezeichnung**</dt> </dl>    | Gibt das umgebende Rechteck des Unterelement Texts zurück.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

