---
title: EM_GETIMEMODEBIAS (Richedit.h)
description: Ruft den ImE-Modus (Input Method Editor) für ein Microsoft Rich Edit-Steuerelement ab.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad5504ca2e5ac1a332657c4f539c9f983292617b6e74b949598488ceb38dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019538"
---
# <a name="em_getimemodebias-message"></a>EM \_ GETIMEMODEBIAS-Nachricht

Ruft den ImE-Modus (Input Method Editor) für ein Microsoft Rich Edit-Steuerelement ab.

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

Diese Meldung gibt die aktuelle ImE-Modus-Biaseinstellung zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie EM [**\_ GETCTFMODEBIAS,**](em-getctfmodebias.md)um den Textdienstframework modus zu erhalten.

Die Anwendung sollte [**EM \_ ISIME vor dem**](em-isime.md) Aufrufen dieser Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> </dl>

 

 





