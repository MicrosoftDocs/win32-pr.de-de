---
title: EM_GETTEXTMODE Meldung (RichEdit. h)
description: Ruft den aktuellen Textmodus und die rückgängig-Ebene eines Rich-Edit-Steuer Elements ab.
ms.assetid: 5c976a82-9c51-4700-9db4-a6b0ed7bb852
keywords:
- Windows-Steuerelemente für EM_GETTEXTMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 012a12aec573518c859ec7f2a0319036dcd1ef87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478114"
---
# <a name="em_gettextmode-message"></a>EM \_ gettextmode-Meldung

Ruft den aktuellen Textmodus und die rückgängig-Ebene eines Rich-Edit-Steuer Elements ab.

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

Der Rückgabewert ist ein oder mehrere Werte aus dem [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) -Enumerationstyp. Die Werte geben den aktuellen Textmodus und die rückgängig-Ebene des Steuer Elements an.

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

[**EM \_ settextmode**](em-settextmode.md)
</dt> <dt>

[**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> </dl>

 

 





