---
title: UDM_GETACCEL Meldung (Commctrl.h)
description: Ruft Beschleunigungsinformationen für ein Auf-Ab-Steuerelement ab.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3603f364a6caa4f4726460e4b5b71e0d79564fbe9178414576fbed2ce5f5777d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132190"
---
# <a name="udm_getaccel-message"></a>UDM \_ GETACCEL-Nachricht

Ruft Beschleunigungsinformationen für ein Auf-Ab-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Anzahl der Elemente im Array, die von *lParam* angegeben werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf ein Array von [**UDACCEL-Strukturen,**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) die Beschleunigungsinformationen empfangen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl von Zugriffstasten, die derzeit für das Steuerelement festgelegt sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**UDM \_ SETACCEL**](udm-setaccel.md)
</dt> </dl>

 

 





