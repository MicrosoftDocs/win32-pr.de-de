---
title: EM_SEARCHWEB Meldung (Commctrl.h)
description: Öffnet den Browser und führt eine Websuche mit dem ausgewählten Text als Suchbegriff aus.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21523df67acf91b8a44f59ea40b012f1af7c287185b7ac64b5dc1288005dfb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673176"
---
# <a name="em_searchweb-message"></a>EM \_ SEARCHWEB-Nachricht

Öffnet den Browser und führt eine Websuche mit dem ausgewählten Text als Suchbegriff aus.

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

## <a name="remarks"></a>Hinweise

Wenn das Feature "Web durchsuchen" mithilfe der [**EM \_ ENABLESEARCHWEB-Nachricht**](em-enablesearchweb.md) deaktiviert ist, hat diese Meldung keine Auswirkungen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur 1809 \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2019-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> </dl>

 

 





