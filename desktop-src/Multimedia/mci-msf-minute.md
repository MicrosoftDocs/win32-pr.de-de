---
title: MCI_MSF_MINUTE -Makro (Mciapi.h)
description: Das MCI MSF MINUTE-Makro ruft die Minutenkomponente aus einem Parameter ab, der gepackte \_ \_ MSF-Informationen (Minutes/Seconds/Frames) enthält.
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE-Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8423e63c7e155c072b496a9bf13c332619f96e8c6780cac6fae266f6a924c9f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039140"
---
# <a name="mci_msf_minute-macro"></a>\_MCI-MSF \_ MINUTE-Makro

Das **MCI \_ MSF \_ MINUTE-Makro** ruft die Minutenkomponente aus einem Parameter ab, der gepackte MSF-Informationen (Minutes/Seconds/Frames) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwMSF* 
</dt> <dd>

Zeit im MSF-Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Minutenkomponente der angegebenen MSF-Informationen zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im MSF-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Minuten, dem nächsten am wenigsten signifikanten Byte mit Sekunden und dem nächsten am wenigsten signifikanten Byte ausgedrückt, das Frames enthält. Das wichtigste Byte wird nicht verwendet.

Das **MCI \_ MSF \_ MINUTE-Makro** ist wie folgt definiert:


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
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

 

 





