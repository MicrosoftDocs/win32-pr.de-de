---
title: TVM_GETIMAGELIST Nachricht (Commctrl.h)
description: Ruft das Handle der Normalen- oder Zustandsbildliste ab, die einem Strukturansichtssteuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetImageList-Makros senden.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- TVM_GETIMAGELIST Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 2b7536f21757d5ad03446654d9eed17444e4e07570c3f4bf032b7d32f0009208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293280"
---
# <a name="tvm_getimagelist-message"></a>TVM \_ GETIMAGELIST-Nachricht

Ruft das Handle der Normalen- oder Zustandsbildliste ab, die einem Strukturansichtssteuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetImageList-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Typ der abzurufende Bildliste. Dieser Parameter kann einer der folgenden Werte sein:



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ NORMAL**</dt> </dl> | Gibt die normale Bildliste an, die ausgewählte, nicht ausgewählte und Überlagerungsbilder für die Elemente eines Strukturansichtssteuerelements enthält.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**TVSIL \_ STATE**</dt> </dl>    | Gibt die Statusbildliste an. Sie können Zustandsbilder verwenden, um anwendungsdefinierte Elementzustände anzugeben. Links neben dem ausgewählten oder nicht ausgewählten Bild eines Elements wird ein Zustandsbild angezeigt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt ein HIMAGELIST-Handle für die angegebene Bildliste zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TVM \_ SETIMAGELIST**](tvm-setimagelist.md)
</dt> </dl>

 

 





