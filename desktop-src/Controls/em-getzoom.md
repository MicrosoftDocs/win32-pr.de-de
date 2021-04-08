---
title: EM_GETZOOM Meldung (RichEdit. h)
description: Ruft das aktuelle Zoomverhältnis ab. Die Zoom-Ration liegt immer zwischen 1/64 und 64. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- Windows-Steuerelemente für EM_GETZOOM Meldung
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740296"
---
# <a name="em_getzoom-message"></a>EM \_ getzoom-Meldung

Ruft das aktuelle Zoomverhältnis eines mehrzeiligen Bearbeitungs Steuer Elements oder eines Rich-Edit-Steuer Elements ab. Die Zoom-Ration liegt immer zwischen 1/64 und 64.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Empfängt den Zähler des Zoom Verhältnisses.

</dd> <dt>

*lParam* 
</dt> <dd>

Empfängt den Nenner des Zoom Verhältnisses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt **true** zurück, wenn die Nachricht verarbeitet wird. Dies ist, wenn sowohl *wParam* als auch *LPARAM* nicht **null** sind.

## <a name="remarks"></a>Bemerkungen

**Bearbeiten:** Wird in Windows 10 1809 und höher unterstützt. Das Bearbeitungs Steuerelement muss über den erweiterten Stil des **es \_ Ex \_** -Formats verfügen, damit diese Nachricht wirksam wird. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md). Weitere Informationen zum Bearbeitungs Steuerelement finden Sie unter [Edit Controls](edit-controls.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h/kommctrl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ setzoom**](em-setzoom.md)
</dt> </dl>

 

 





