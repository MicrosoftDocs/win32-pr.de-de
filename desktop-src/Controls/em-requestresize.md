---
title: EM_REQUESTRESIZE Meldung (RichEdit. h)
description: Erzwingt, dass ein RichEdit-Steuerelement einen en \_ RequestResize-Benachrichtigungs Code an das übergeordnete Fenster sendet.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- Windows-Steuerelemente für EM_REQUESTRESIZE Meldung
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec41e7be8e0f30d5c1ec011247f3964292c2218e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213743"
---
# <a name="em_requestresize-message"></a>EM \_ RequestResize-Meldung

Erzwingt, dass ein RichEdit-Steuerelement einen [**en \_ RequestResize**](en-requestresize.md) -Benachrichtigungs Code an das übergeordnete Fenster sendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ist während der Verarbeitung der [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size) für das übergeordnete Element eines untersten Rich-Edit-Steuer Elements nützlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**de \_ RequestResize**](en-requestresize.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ Größe**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

