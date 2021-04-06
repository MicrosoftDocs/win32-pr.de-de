---
title: TVM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft das Handle für die normale oder Zustands Bildliste ab, die einem Strukturansicht-Steuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetImageList-Makros senden.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- Windows-Steuerelemente für TVM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743392"
---
# <a name="tvm_getimagelist-message"></a>TVM \_ GetImageList-Meldung

Ruft das Handle für die normale oder Zustands Bildliste ab, die einem Strukturansicht-Steuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Typ der abzurufenden Bildliste. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**tvsil \_ Normal**</dt> </dl> | Gibt die normale Bildliste an, die ausgewählte, nicht ausgewählte und Überlagerungs Bilder für die Elemente eines Strukturansicht-Steuer Elements enthält.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**tvsil- \_ Status**</dt> </dl>    | Gibt die Status Bild Liste an. Sie können Zustands Bilder verwenden, um Anwendungs definierte Element Zustände anzugeben. Links neben dem ausgewählten oder nicht ausgewählten Bild eines Elements wird ein Status Bild angezeigt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein HIMAGELIST-Handle für die angegebene Bildliste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ SetImageList**](tvm-setimagelist.md)
</dt> </dl>

 

 





