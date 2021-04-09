---
title: EM_SETHYPHENATEINFO Meldung (RichEdit. h)
description: Legt die Methode fest, mit der ein Rich-Edit-Steuerelement eine Bindestriche hat
ms.assetid: 67126cb8-ab50-49a9-b32f-2245debf2fe3
keywords:
- Windows-Steuerelemente für EM_SETHYPHENATEINFO Meldung
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
ms.openlocfilehash: b8369d463ae03e9410347ab58a50346625e3de47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859172"
---
# <a name="em_sethyphenateinfo-message"></a>EM- \_ logphenateinfo-Nachricht

Legt die Methode fest, mit der ein Rich-Edit-Steuerelement eine Bindestriche hat

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine [**hyphenateingefo**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) -Struktur.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet, muss 0 (null) sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um die Bindestriche zu aktivieren, muss der Client " [**EM \_ settypographyoptions**](em-settypographyoptions.md)" aufzurufen, wobei " \_ advancedtypografie" angegeben wird.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ gethyphenateingefo**](em-gethyphenateinfo.md)
</dt> </dl>

 

 





