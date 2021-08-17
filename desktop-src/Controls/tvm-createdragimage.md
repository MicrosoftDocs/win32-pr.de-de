---
title: TVM_CREATEDRAGIMAGE Meldung (Commctrl.h)
description: Erstellt eine Ziehbitmap für das angegebene Element in einem Strukturansichtssteuerelement.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: a18a00b2225749b30b8dcd9a928fd73e3ffabcfd4a4f9512cd2332d98cc08a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408660"
---
# <a name="tvm_createdragimage-message"></a>TVM \_ CREATEDRAGIMAGE-Nachricht

Erstellt eine Ziehbitmap für das angegebene Element in einem Strukturansichtssteuerelement. Die Nachricht erstellt auch eine Bildliste für die Bitmap und fügt die Bitmap der Bildliste hinzu. Eine Anwendung kann das Bild anzeigen, wenn das Element mithilfe der Bildlistenfunktionen gezogen wird. Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ CreateDragImage-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Element, das die neue Ziehbitmap empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Bildliste zurück, zu der die Ziehbitmap hinzugefügt wurde, falls erfolgreich, oder **andernfalls NULL.**

## <a name="remarks"></a>Hinweise

Wenn Sie ein Strukturansichtssteuerelement ohne zugeordnete Bildliste erstellen, können Sie die **TVM \_ CREATEDRAGIMAGE-Nachricht** nicht verwenden, um das Bild zu erstellen, das während eines Ziehvorgangs angezeigt werden soll. Sie müssen Ihre eigene Methode zum Erstellen eines Ziehcursors implementieren.

Ihre Anwendung ist dafür verantwortlich, die Imageliste zu zerstören, wenn sie nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





