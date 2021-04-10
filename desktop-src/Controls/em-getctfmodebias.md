---
title: EM_GETCTFMODEBIAS Meldung (RichEdit. h)
description: Ruft die biaswerte des Text Dienste-frameworkmodus für ein Microsoft Rich Edit-Steuerelement ab.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Windows-Steuerelemente für EM_GETCTFMODEBIAS Meldung
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104042"
---
# <a name="em_getctfmodebias-message"></a>EM \_ getctf modebias-Nachricht

Ruft die biaswerte des Text Dienste-frameworkmodus für ein Microsoft Rich Edit-Steuerelement ab.

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

Der aktuelle Wert des Text Services-frameworkmodus.

## <a name="remarks"></a>Bemerkungen

Um die Verschiebung des IME-Modus abzurufen, aufrufen Sie [**EM \_ getimemodebias**](em-getimemodebias.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ setctf modebias**](em-setctfmodebias.md)
</dt> <dt>

[**EM \_ getimemodebias**](em-getimemodebias.md)
</dt> </dl>

 

 





