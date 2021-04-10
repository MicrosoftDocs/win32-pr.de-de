---
title: EM_GETOPTIONS Meldung (RichEdit. h)
description: Ruft Optionen für Rich-Edit-Steuerelemente ab.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- Windows-Steuerelemente für EM_GETOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956821"
---
# <a name="em_getoptions-message"></a>EM \_ GetOptions-Meldung

Ruft Optionen für Rich-Edit-Steuerelemente ab.

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

Diese Meldung gibt eine Kombination der aktuellen optionsflagwerte zurück, die in der [**EM- \_ SetOptions**](em-setoptions.md) -Nachricht beschrieben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ toptions**](em-setoptions.md)
</dt> </dl>

 

 





