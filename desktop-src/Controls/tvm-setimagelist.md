---
title: TVM_SETIMAGELIST Meldung (kommstrg. h)
description: Legt die normale oder Zustands Bildliste für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement mithilfe der neuen Bilder neu. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetImageList-Makros senden.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- Windows-Steuerelemente für TVM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741553"
---
# <a name="tvm_setimagelist-message"></a>TVM \_ SetImageList-Meldung

Legt die normale oder Zustands Bildliste für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement mithilfe der neuen Bilder neu. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Typ der festzulegenden Bildliste. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**tvsil \_ Normal**</dt> </dl> | Gibt die normale Bildliste an, die ausgewählte, nicht ausgewählte und Überlagerungs Bilder für die Elemente eines Strukturansicht-Steuer Elements enthält.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**tvsil- \_ Status**</dt> </dl>    | Gibt die Status Bild Liste an. Sie können Zustands Bilder verwenden, um Anwendungs definierte Element Zustände anzugeben. Links neben dem ausgewählten oder nicht ausgewählten Bild eines Elements wird ein Status Bild angezeigt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die Bildliste. Wenn *LPARAM* den Wert **null** hat, entfernt die Meldung die angegebene Bildliste aus dem Strukturansicht-Steuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ggf. das Handle für die vorherige Bildliste zurück, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Das Strukturansicht-Steuerelement zerstört nicht die mit dieser Meldung angegebene Bildliste. Die Anwendung muss die Bildliste zerstören, wenn Sie nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GetImageList**](tvm-getimagelist.md)
</dt> </dl>

 

 





