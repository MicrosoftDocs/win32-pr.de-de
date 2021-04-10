---
title: MCI_HMS_HOUR-Makro (mciapi. h)
description: Das MCI \_ - \_ Element "HMS Hour" Ruft die Stunden Komponente von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040987"
---
# <a name="mci_hms_hour-macro"></a>MCI- \_ HMS- \_ Stunden-Makro

Das **MCI-Element " \_ HMS \_ Hour** " Ruft die Stunden Komponente von einem Parameter ab, der gepackte Stunden/Minuten/Sekunden (HMS) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_HMS_HOUR(
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

Gibt die Stunden Komponente der angegebenen HMS-Informationen zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt. Das signifikanteste Byte wird nicht verwendet.

Das **MCI-Element " \_ HMS \_ Hour** " ist wie folgt definiert:


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
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

 

 





