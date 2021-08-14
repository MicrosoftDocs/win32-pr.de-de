---
title: LVM_CREATEDRAGIMAGE (Commctrl.h)
description: Erstellt eine Ziehbildliste für das angegebene Element. Sie können diese Nachricht explizit oder mithilfe des ListView \_ CreateDragImage-Makros senden.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE von Windows Steuerelementen
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d551dfa7b14ecff8c9fd1efe015e173403c1b5981f294a18b3180a42cc03de63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411996"
---
# <a name="lvm_createdragimage-message"></a>LVM \_ CREATEDRAGIMAGE-Nachricht

Erstellt eine Ziehbildliste für das angegebene Element. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ CreateDragImage-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**POINT-Struktur,**](/previous-versions//dd162805(v=vs.85)) die die ursprüngliche Position der oberen linken Ecke des Bilds in Ansichtskoordinaten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle an die Ziehbildliste zurück, falls erfolgreich, **andernfalls NULL.**

## <a name="remarks"></a>Hinweise

Ihre Anwendung ist dafür verantwortlich, die Bildliste zu zerstören, wenn sie nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

