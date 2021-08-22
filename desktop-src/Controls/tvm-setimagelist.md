---
title: TVM_SETIMAGELIST-Nachricht (Commctrl.h)
description: Legt die Normale- oder Zustandsbildliste für ein Strukturansichtssteuerelement fest und zeichnet das Steuerelement mithilfe der neuen Bilder neu. Sie können diese Nachricht explizit oder mithilfe des \_ TreeView-Makros SetImageList senden.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: df79089c7a2071c6af702da9ef862178738ede3dccff312c3fbae7dbefe4de56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018678"
---
# <a name="tvm_setimagelist-message"></a>TVM \_ SETIMAGELIST-Nachricht

Legt die Normale- oder Zustandsbildliste für ein Strukturansichtssteuerelement fest und zeichnet das Steuerelement mithilfe der neuen Bilder neu. Sie können diese Nachricht explizit oder mithilfe des [**\_ TreeView-Makros SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Typ der festzulegende Bildliste. Dieser Parameter kann einer der folgenden Werte sein:



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ NORMAL**</dt> </dl> | Gibt die normale Bildliste an, die ausgewählte, nicht ausgewählte und Überlagerungsbilder für die Elemente eines Strukturansichtssteuerelements enthält.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**TVSIL \_ STATE**</dt> </dl>    | Gibt die Statusbildliste an. Sie können Zustandsbilder verwenden, um anwendungsdefinierte Elementzustände anzugeben. Links neben dem ausgewählten oder nicht ausgewählten Bild eines Elements wird ein Zustandsbild angezeigt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für die Bildliste. Wenn *lParam* **NULL** ist, entfernt die Nachricht die angegebene Bildliste aus dem Strukturansichtssteuerelement.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die vorherige Bildliste zurück, sofern vorhanden, oder **andernfalls NULL.**

## <a name="remarks"></a>Hinweise

Das Strukturansichtssteuerelement zerstört nicht die mit dieser Meldung angegebene Bildliste. Ihre Anwendung muss die Imageliste zerstören, wenn sie nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TVM \_ GETIMAGELIST**](tvm-getimagelist.md)
</dt> </dl>

 

 





