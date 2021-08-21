---
title: MCI_MSF_SECOND-Makro (Mciapi.h)
description: Das MCI MSF SECOND-Makro ruft die Sekundenkomponente aus einem Parameter ab, der gepackte \_ \_ MSF-Informationen (Minutes/Seconds/Frames) enthält.
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND-Makros Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb09643ae8d3ecdf59c6f3631c9dc28f43bba7ee0434ebabed3e4260c3fec01d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138359"
---
# <a name="mci_msf_second-macro"></a>MCI \_ MSF \_ SECOND-Makro

Das **MCI \_ MSF \_ SECOND-Makro** ruft die Sekundenkomponente aus einem Parameter ab, der gepackte MSF-Informationen (Minutes/Seconds/Frames) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_MSF_SECOND(
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

Gibt die Sekundenkomponente der angegebenen MSF-Informationen zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im MSF-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Minuten, dem nächsten am wenigsten signifikanten Byte mit Sekunden und dem nächsten am wenigsten signifikanten Byte ausgedrückt, das Frames enthält. Das wichtigste Byte wird nicht verwendet.

Das **MCI \_ MSF \_ SECOND-Makro** ist wie folgt definiert:


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
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

 

 





