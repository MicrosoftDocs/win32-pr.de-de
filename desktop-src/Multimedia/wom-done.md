---
title: WOM_DONE Meldung (MMSYSTEM. h)
description: '\_Wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird, wird die gesendete WOM-Nachricht an eine "Waveform-Audioausgabe"-Rückruffunktion gesendet.'
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103026"
---
# <a name="wom_done-message"></a>WOM- \_ done-Nachricht

Wenn der angegebene Ausgabepuffer an die Anwendung zurückgegeben wird, wird die gesendete **WOM \_** -Nachricht an eine "Waveform-Audioausgabe"-Rückruffunktion gesendet. Puffer werden an die Anwendung zurückgegeben, wenn Sie abgespielt wurden, oder als Ergebnis eines Aufrufes der [**wavesetzset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) -Funktion.


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Zeiger auf eine [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die den Puffer identifiziert.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Bleiben muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Waveform-Audiodatei](waveform-audio.md)
</dt> <dt>

[Wellenform Meldungen](waveform-messages.md)
</dt> </dl>

 

