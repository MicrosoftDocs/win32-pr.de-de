---
title: MCI_MAKE_HMS-Makro (mciapi. h)
description: Das MCI \_ -Element "Make \_ HMS" erstellt einen Zeitwert im Format "gepackte Stunden/Minuten/Sekunden" (HMS) aus den angegebenen Stunden, Minuten und Sekunden Werten.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743144"
---
# <a name="mci_make_hms-macro"></a>MCI-Element " \_ \_ HMS"

Das **MCI-Element " \_ make \_ HMS** " erstellt einen Zeitwert im Format "gepackte Stunden/Minuten/Sekunden" (HMS) aus den angegebenen Stunden, Minuten und Sekunden Werten.

## <a name="syntax"></a>Syntax


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hours* 
</dt> <dd>

Anzahl der Stunden.

</dd> <dt>

*minutes* 
</dt> <dd>

Anzahl der Minuten.

</dd> <dt>

*Sekunden* 
</dt> <dd>

Anzahl der Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeit im gepackten HMS-Format zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt. Das signifikanteste Byte wird nicht verwendet.

Das **MCI-Element " \_ make \_ HMS** " ist wie folgt definiert:


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Makros](mci-macros.md)
</dt> </dl>

 

 





