---
title: MCI_TMSF_TRACK Makro (Mciapi.h)
description: Das MCI \_ TMSF \_ TRACK-Makro ruft die Trackkomponente aus einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF)-Informationen enthält.
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK-Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7090a2a9b652d7c989aadd70d8843ece04bf467bbbe353c22c3f76fee8a9712b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137951"
---
# <a name="mci_tmsf_track-macro"></a>MCI \_ TMSF \_ TRACK-Makro

Das **MCI \_ TMSF \_ TRACK-Makro** ruft die Trackkomponente aus einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF)-Informationen enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwTMSF* 
</dt> <dd>

Zeit im TMSF-Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Trackkomponente der angegebenen TMSF-Informationen zurück.

## <a name="remarks"></a>Hinweise

Die Zeit im TMSF-Format wird als **DWORD-Wert** mit dem am wenigsten signifikanten Byte mit Spuren, dem nächstwertigsten Byte mit Minuten, dem nächstwertigsten Byte, das Sekunden enthält, und dem wichtigsten Byte, das Frames enthält, ausgedrückt.

Das **MCI \_ TMSF \_ TRACK-Makro** ist wie folgt definiert:


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
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

 

 





