---
title: MCI_HMS_SECOND Makro (Mciapi.h)
description: Das MCI \_ HMS \_ SECOND-Makro ruft die Sekundenkomponente aus einem Parameter ab, der gepackte Informationen zu Stunden/Minuten/Sekunden (HMS) enthält.
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND-Makro Windows Multimedia
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
ms.openlocfilehash: bc61747d891d3c91afd5e4cb7f9a16eef44e13eb3de275bbf9575d8a4f584d40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039230"
---
# <a name="mci_hms_second-macro"></a>MCI \_ HMS \_ SECOND-Makro

Das **MCI \_ HMS \_ SECOND-Makro** ruft die Sekundenkomponente aus einem Parameter ab, der gepackte Informationen zu Stunden/Minuten/Sekunden (HMS) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_HMS_SECOND(
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

Gibt die Sekundenkomponente der angegebenen HMS-Informationen zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im HMS-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Stunden, dem nächstwertigen Byte mit Minuten und dem nächstletzten Byte mit Sekunden ausgedrückt. Das wichtigste Byte wird nicht verwendet.

Das **MCI \_ HMS \_ SECOND-Makro** ist wie folgt definiert:


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
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

 

 





