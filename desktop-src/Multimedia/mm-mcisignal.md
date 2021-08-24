---
title: MM_MCISIGNAL Meldung (Mmsystem.h)
description: Die MM \_ MCISIGNAL-Nachricht wird an ein Fenster gesendet, um eine Anwendung darüber zu informieren, dass ein MCI-Gerät eine position erreicht hat, die in einem vorherigen Signal (MCI \_ SIGNAL)-Befehl definiert wurde.
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb54b56d35ad34d10d95c2a34b52b370fb856d9c958dd42223c7f0a08ddbdfb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807440"
---
# <a name="mm_mcisignal-message"></a>\_MM-MCISIGNAL-Nachricht

Die **MM \_ MCISIGNAL-Nachricht** wird an ein Fenster gesendet, um eine Anwendung darüber zu informieren, dass ein MCI-Gerät eine position erreicht hat, die in einem vorherigen [**Signalbefehl**](signal.md) [**(MCI \_ SIGNAL**](mci-signal.md)) definiert wurde.


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*Wid*
</dt> <dd>

Bezeichner des Geräts, das die Signalmeldung initiiert.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Wert, der im **dwUserParm-Member** der **\_ MCI-DGV \_ SIGNAL \_ PARAMS-Struktur** übergeben wird, wenn der **Signalbefehl** diese Rückruffunktion definiert hat. Alternativ kann er den Positionswert enthalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Nachrichten](mci-messages.md)
</dt> <dt>

[**Signal**](signal.md)
</dt> </dl>

 

 





