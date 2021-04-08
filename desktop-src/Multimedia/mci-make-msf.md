---
title: MCI_MAKE_MSF-Makro (mciapi. h)
description: Das MCI \_ make \_ MSF-Makro erstellt einen Zeitwert im MSF-Format (gepackt Minutes/seconds/Frames) aus den angegebenen Minuten, Sekunden und Frame Werten.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957161"
---
# <a name="mci_make_msf-macro"></a>MCI- \_ make \_ MSF-Makro

Das **MCI \_ make \_ MSF** -Makro erstellt einen Zeitwert im MSF-Format (gepackt Minutes/seconds/Frames) aus den angegebenen Minuten, Sekunden und Frame Werten.

## <a name="syntax"></a>Syntax


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*minutes* 
</dt> <dd>

Anzahl der Minuten.

</dd> <dt>

*Sekunden* 
</dt> <dd>

Anzahl der Sekunden.

</dd> <dt>

*SSE* 
</dt> <dd>

Anzahl der Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeit im gepackten MSF-Format zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im MSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Minuten enthält, dem nächst bedeutsamen Byte, das Sekunden enthält, und dem nächstniedrigsten Byte mit Frames ausgedrückt. Das signifikanteste Byte wird nicht verwendet.

Das **MCI- \_ make- \_ MSF** -Makro wird wie folgt definiert:


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
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

 

 





