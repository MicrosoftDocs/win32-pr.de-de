---
title: TVM_CREATEDRAGIMAGE Meldung (kommstrg. h)
description: Erstellt eine Zieh Bitmap für das angegebene Element in einem Strukturansicht-Steuerelement.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- Windows-Steuerelemente für TVM_CREATEDRAGIMAGE Meldung
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103904"
---
# <a name="tvm_createdragimage-message"></a>TVM- \_ Meldung "fiatedragimage"

Erstellt eine Zieh Bitmap für das angegebene Element in einem Strukturansicht-Steuerelement. Die Meldung erstellt außerdem eine Bildliste für die Bitmap und fügt der Bildliste die Bitmap hinzu. Eine Anwendung kann das Bild anzeigen, wenn Sie das Element mithilfe der ImageList-Funktionen ziehen. Sie können diese Nachricht explizit oder mithilfe des [**TreeView-Makros " \_ kreeview**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Element, das die neue Zieh Bitmap empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, der die Zieh Bitmap hinzugefügt wurde, wenn erfolgreich, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Strukturansicht-Steuerelement ohne zugeordnete Bildliste erstellen, können Sie das Bild, das während eines Zieh Vorgangs angezeigt wird, nicht mithilfe der TVM-Meldung " **\_ fiatedragimage** " erstellen. Sie müssen eine eigene Methode zum Erstellen eines Zieh Cursors implementieren.

Die Anwendung ist dafür verantwortlich, die Bildliste zu zerstören, wenn Sie nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





