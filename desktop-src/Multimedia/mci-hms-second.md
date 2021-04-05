---
title: MCI_HMS_SECOND-Makro (mciapi. h)
description: Das MCI-Element für die \_ HMS \_ -Sekunde ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen zu den gepackten Stunden/Minuten/Sekunden (
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859273"
---
# <a name="mci_hms_second-macro"></a>MCI- \_ HMS- \_ zweites Makro

Das MCI-Element für die **\_ HMS- \_ Sekunde** Ruft die Sekunden Komponente von einem Parameter ab, der die Informationen zu den Informationen zu den gepackten Stunden/Minuten/Sekunden (

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_HMS_SECOND(
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

Gibt die Sekunden Komponente der angegebenen HMS-Informationen zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im "HMS"-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das Stunden enthält, dem nächst bedeutsamen Byte, das Minuten enthält, und dem nächstniedrigsten Byte mit Sekunden ausgedrückt. Das signifikanteste Byte wird nicht verwendet.

Das **MCI-Element " \_ HMS \_ Second** " ist wie folgt definiert:


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
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

 

 





