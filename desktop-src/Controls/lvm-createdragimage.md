---
title: LVM_CREATEDRAGIMAGE Meldung (kommstrg. h)
description: Erstellt eine Ziehbild Liste für das angegebene Element. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros "auflistungdragimage" senden.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Windows-Steuerelemente für LVM_CREATEDRAGIMAGE Meldung
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
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102906"
---
# <a name="lvm_createdragimage-message"></a>LVM-Nachricht für " \_ kreatedragimage"

Erstellt eine Ziehbild Liste für das angegebene Element. Sie können diese Nachricht explizit oder mithilfe des ListView-Makros " [**auflistungdragimage \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) " senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Index des Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die ursprüngliche Position der oberen linken Ecke des Bilds in Ansichts Koordinaten empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für die Drag-Bildliste zurück, wenn erfolgreich, andernfalls **null** .

## <a name="remarks"></a>Bemerkungen

Die Anwendung ist dafür verantwortlich, die Bildliste zu zerstören, wenn Sie nicht mehr benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

