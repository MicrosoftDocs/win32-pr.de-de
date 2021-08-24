---
title: LVM_GETIMAGELIST (Commctrl.h)
description: Ruft das Handle für eine Bildliste ab, die zum Zeichnen von Listenansichtselementen verwendet wird. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetImageList-Makros senden.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- LVM_GETIMAGELIST message Windows Controls
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
ms.openlocfilehash: 339de36c85b4a5d39476a93cde71cbc6db23d1bc08946d3ce2d1ab1b5a4cb926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540810"
---
# <a name="lvm_getimagelist-message"></a>LVM \_ GETIMAGELIST-Nachricht

Ruft das Handle für eine Bildliste ab, die zum Zeichnen von Listenansichtselementen verwendet wird. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetImageList-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Bildliste, die abgerufen werden soll. Dieser Parameter kann einen der folgenden Werte haben:



| Wert                                                                                                                                                                     | Bedeutung                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ NORMAL**</dt> </dl>                | Bildliste mit großen Symbolen.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ SMALL**</dt> </dl>                   | Bildliste mit kleinen Symbolen.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**LVSIL \_ STATE**</dt> </dl>                   | Bildliste mit Zustandsbildern.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**LVSIL \_ GROUPHEADER**</dt> </dl> | Bildliste für Gruppenheader.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle bei Erfolg an die angegebene Bildliste zurück, **andernfalls NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





