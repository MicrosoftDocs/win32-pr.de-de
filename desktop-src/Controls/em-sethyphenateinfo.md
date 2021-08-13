---
title: EM_SETHYPHENATEINFO (Richedit.h)
description: Legt fest, wie ein Rich-Edit-Steuerelement Bindestriche vorsteuert.
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- EM_SETHYPHENATEINFO von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_SETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5551aace3ab054c1c6fa322242ae06386ff19f5a44775bd6dcc6887d19c65c62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437560"
---
# <a name="em_sethyphenateinfo-message"></a>EM \_ SETHYPHENATEINFO-Nachricht

Legt fest, wie ein Rich-Edit-Steuerelement Bindestriche vorsteuert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine [**HYPHENATEINFO-Struktur.**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo)

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet, muss 0 (null) sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um Bindestriche zu aktivieren, muss der Client [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)aufrufen und TO \_ ADVANCEDTYPOGRAPHY angeben.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**EM \_ GETHYPHENATEINFO**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





