---
title: MCI_TMSF_SECOND-Makro (Mciapi.h)
description: Das MCI TMSF SECOND-Makro ruft die Sekundenkomponente aus einem Parameter ab, der gepackte \_ \_ TmSF-Informationen (Tracks/Minutes/Seconds/Frames) enthält.
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND-Makros Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92dc8f7771df35e9ddc712d263e805ba1e844ca42cde607d7204dc6dc7b350d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784199"
---
# <a name="mci_tmsf_second-macro"></a>MCI \_ TMSF \_ SECOND-Makro

Das **MCI \_ TMSF \_ SECOND-Makro** ruft die Sekundenkomponente aus einem Parameter ab, der gepackte TmSF-Informationen (Tracks/Minutes/Seconds/Frames) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_TMSF_SECOND(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwTMSF* 
</dt> <dd>

Uhrzeit im TMSF-Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Sekundenkomponente der angegebenen TMSF-Informationen zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im TMSF-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Spuren, dem nächsten am wenigsten signifikanten Byte mit Minuten, dem nächsten am wenigsten signifikanten Byte mit Sekunden und dem signifikantesten Byte ausgedrückt, das Frames enthält.

Das **MCI \_ TMSF \_ SECOND-Makro** ist wie folgt definiert:


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Makros](mci-macros.md)
</dt> </dl>

 

 





