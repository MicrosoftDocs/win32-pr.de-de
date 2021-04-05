---
title: MCI_TMSF_TRACK-Makro (mciapi. h)
description: Das MCI \_ TMSF \_ Track-Makro ruft die Track-Komponente von einem Parameter ab, der gepackte Titel/Minuten/Sekunden/Frames (TMSF) enthält.
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK Makro Windows Multimedia
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
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858956"
---
# <a name="mci_tmsf_track-macro"></a>MCI \_ TMSF- \_ Track-Makro

Das **MCI \_ TMSF \_ Track** -Makro ruft die Track-Komponente von einem Parameter ab, der gepackte Titel/Minuten/Sekunden/Frames (TMSF) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwtmsf* 
</dt> <dd>

Zeit im TMSF-Format.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Spuren Komponente der angegebenen TMSF-Informationen zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.

Das **MCI \_ TMSF \_ Track** -Makro wird wie folgt definiert:


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
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

 

 





