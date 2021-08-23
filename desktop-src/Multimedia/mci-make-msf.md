---
title: MCI_MAKE_MSF-Makro (Mciapi.h)
description: Das MSF-Makro MCI MAKE erstellt einen Zeitwert im \_ MSF-Format (Gepackte Minuten/Sekunden/Frames) aus den angegebenen Minuten-, Sekunden- \_ und Framewerten.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF-Makros Windows Multimedia
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
ms.openlocfilehash: e16f5cfa2b99f7bdbd7eb3029b3f0186904d8b8e94f455614464fadc98cdd20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690130"
---
# <a name="mci_make_msf-macro"></a>MCI \_ MAKE \_ MSF-Makro

Das **\_ \_ MSF-Makro MCI MAKE** erstellt einen Zeitwert im MSF-Format (Gepackte Minuten/Sekunden/Frames) aus den angegebenen Minuten-, Sekunden- und Framewerten.

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

*Frames* 
</dt> <dd>

Anzahl von Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeit im gepackten MSF-Format zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im MSF-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Minuten, dem nächsten am wenigsten signifikanten Byte mit Sekunden und dem nächsten am wenigsten signifikanten Byte ausgedrückt, das Frames enthält. Das wichtigste Byte wird nicht verwendet.

Das **\_ \_ MSF-Makro MCI MAKE** ist wie folgt definiert:


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
| Header<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Makros](mci-macros.md)
</dt> </dl>

 

 





