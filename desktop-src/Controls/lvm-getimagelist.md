---
title: LVM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft das Handle für eine Bildliste ab, die zum Zeichnen von Listen Ansichts Elementen verwendet wird. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetImageList-Makros senden.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Windows-Steuerelemente für LVM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104451"
---
# <a name="lvm_getimagelist-message"></a>LVM \_ GetImageList-Meldung

Ruft das Handle für eine Bildliste ab, die zum Zeichnen von Listen Ansichts Elementen verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Abzurufende Bildliste. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                     | Bedeutung                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**lvsil \_ Normal**</dt> </dl>                | Bildliste mit großen Symbolen.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**lvsil \_ Small**</dt> </dl>                   | Bildliste mit kleinen Symbolen.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**Zustand "lvsil" \_**</dt> </dl>                   | Bildliste mit Zustands Bildern.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**lvsil- \_ GroupHeader**</dt> </dl> | Bildliste für Gruppen Kopfzeile.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die angegebene Bildliste zurück, wenn erfolgreich, andernfalls **null** .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





