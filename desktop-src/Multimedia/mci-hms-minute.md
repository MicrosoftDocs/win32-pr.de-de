---
title: MCI_HMS_MINUTE-Makro (mciapi. h)
description: Das MCI \_ - \_ Element "HMS Minute" Ruft die Komponente "Minutes" von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106209"
---
# <a name="mci_hms_minute-macro"></a>MCI-nach-oben- \_ \_ Makro

Das **MCI-Element " \_ HMS \_ Minute** " Ruft die Komponente "Minutes" von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwhms* 
</dt> <dd>

Zeit im "HMS"-Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Minuten Komponente der angegebenen HMS-Informationen zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt. Das signifikanteste Byte wird nicht verwendet.

Das **MCI-Element " \_ HMS \_ Minute** " ist wie folgt definiert:


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
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

 

 





