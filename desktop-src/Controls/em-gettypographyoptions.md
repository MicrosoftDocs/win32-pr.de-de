---
title: EM_GETTYPOGRAPHYOPTIONS (Richedit.h)
description: Gibt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuerelements zurück.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d575550e2c239ee5b689deb5874a9803c581151b54100ab227a24d4f29941973
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831170"
---
# <a name="em_gettypographyoptions-message"></a>EM \_ GETTYPOGRAPHYOPTIONS-Nachricht

Gibt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuerelements zurück.

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

Gibt die aktuellen Typografieoptionen zurück. Eine Liste der Optionen finden Sie unter [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).

## <a name="remarks"></a>Hinweise

Sie können erweiterte Zeilenumbrüche aktivieren, indem Sie die [**EM \_ SETTYPOGRAPHYOPTIONS-Nachricht**](em-settypographyoptions.md) senden. Erweiterte und normale Zeilenumbrüche können auch automatisch durch das Rich-Edit-Steuerelement aktiviert werden, wenn es für bestimmte Sprachen benötigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Informationen zu Rich Edit-Steuerelementen](about-rich-edit-controls.md)
</dt> </dl>

 

 





