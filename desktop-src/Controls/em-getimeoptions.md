---
title: EM_GETIMEOPTIONS Meldung (RichEdit. h)
description: Ruft die aktuellen IME-Optionen (Input Method Editor) ab.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Windows-Steuerelemente für EM_GETIMEOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104822"
---
# <a name="em_getimeoptions-message"></a>EM \_ getIMEOptions-Meldung

Ruft die aktuellen IME-Optionen (Input Method Editor) ab.

> [!Note]  
> Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie wird in höheren Versionen der Rich-Edit-Version nicht unterstützt.

 

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

Diese Meldung gibt einen oder mehrere der in der Nachricht [**EM \_ setimeoptions**](em-setimeoptions.md) beschriebenen IME-optionsflagwerte zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ Zeit Optionen**](em-setimeoptions.md)
</dt> </dl>

 

 





