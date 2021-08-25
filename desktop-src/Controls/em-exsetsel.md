---
title: EM_EXSETSEL (Richedit.h)
description: Wählt einen Bereich von Zeichen oder Component Object Model (COM)-Objekten in einem Microsoft Rich Edit-Steuerelement aus.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e35840e404f295b7d3ed6ddd5dddf4c77076c236eb3260f6f719b152cef207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915650"
---
# <a name="em_exsetsel-message"></a>EM \_ EXSETSEL-Nachricht

Wählt einen Bereich von Zeichen oder Component Object Model (COM)-Objekten in einem Microsoft Rich Edit-Steuerelement aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**CHARRANGE-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-charrange) die den Auswahlbereich angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Auswahl, die tatsächlich festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





