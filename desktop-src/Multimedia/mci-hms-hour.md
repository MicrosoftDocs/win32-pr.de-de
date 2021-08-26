---
title: MCI_HMS_HOUR Makro (Mciapi.h)
description: Das MCI \_ HMS \_ HOUR-Makro ruft die Stundenkomponente aus einem Parameter ab, der gepackte Informationen zu Stunden/Minuten/Sekunden (HMS) enthält.
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR-Makro Windows Multimedia
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
ms.openlocfilehash: 97b8000e642d18f8499be5f8622a1cf7540fefbd041b7d34f23e1fd5e231815a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039270"
---
# <a name="mci_hms_hour-macro"></a>MCI \_ HMS \_ HOUR-Makro

Das **MCI \_ HMS \_ HOUR-Makro** ruft die Stundenkomponente aus einem Parameter ab, der gepackte Informationen zu Stunden/Minuten/Sekunden (HMS) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwHMS* 
</dt> <dd>

Zeit im HMS-Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Stundenkomponente der angegebenen HMS-Informationen zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im HMS-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Stunden, dem nächstwertigen Byte mit Minuten und dem nächstletzten Byte mit Sekunden ausgedrückt. Das wichtigste Byte wird nicht verwendet.

Das **MCI \_ HMS \_ HOUR-Makro** ist wie folgt definiert:


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Makros](mci-macros.md)
</dt> </dl>

 

 





