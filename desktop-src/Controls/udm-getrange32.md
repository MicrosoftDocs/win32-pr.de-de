---
title: UDM_GETRANGE32 (Commctrl.h)
description: Ruft den 32-Bit-Bereich eines Auf-Ab-Steuerelements ab.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72078327b7a580768321f14c1d512e097561ae3441667497a822dc8a8a28b4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077100"
---
# <a name="udm_getrange32-message"></a>UDM \_ GETRANGE32-Nachricht

Ruft den 32-Bit-Bereich eines Auf-Ab-Steuerelements ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine ganze Zahl mit Vorzeichen, die die Untergrenze des Steuerelementbereichs nach oben empfängt. Dieser Parameter kann NULL **sein.**

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine ganze Zahl mit Vorzeichen, die die Obergrenze des Auf-Ab-Steuerelementbereichs empfängt. Dieser Parameter kann NULL **sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert für diese Meldung wird nicht verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





