---
title: LVM_ARRANGE Meldung (kommstrg. h)
description: Ordnet Elemente in der Symbol Ansicht an. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros anordnen senden.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- Windows-Steuerelemente für LVM_ARRANGE Meldung
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102910"
---
# <a name="lvm_arrange-message"></a>LVM- \_ Anordnungs Nachricht

Ordnet Elemente in der Symbol Ansicht an. Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ anordnen**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Einer der folgenden Werte, der die Ausrichtung angibt:



| Wert                                                                                                                                                            | Bedeutung                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ alignleft**</dt> </dl>    | Nicht implementiert. Wenden Sie stattdessen den [**LVS \_ alignleft**](list-view-window-styles.md) -Stil an.<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ AlignTop**</dt> </dl>       | Nicht implementiert. Verwenden Sie stattdessen den [**LVS \_ AlignTop**](list-view-window-styles.md) -Stil.<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**LVA- \_ Standard**</dt> </dl>          | Richtet Elemente gemäß den aktuellen Ausrichtungs Stilen des Listenansicht-Steuer Elements (Standardwert) aus.<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**LVA- \_ snapragrid**</dt> </dl> | Andoppt alle Symbole an die nächste Raster Position.<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn erfolgreich; andernfalls **false**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





