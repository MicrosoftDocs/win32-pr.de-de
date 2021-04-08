---
title: MCI_TMSF_FRAME-Makro (mciapi. h)
description: Das MCI \_ TMSF- \_ Frame-Makro ruft die Frames-Komponente von einem Parameter ab, der gepackte Titel/Minuten/Sekunden/Frames (TMSF) enthält.
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME Makro Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740256"
---
# <a name="mci_tmsf_frame-macro"></a>MCI \_ TMSF- \_ Frame-Makro

Das **MCI \_ TMSF- \_ Frame** -Makro ruft die Frames-Komponente von einem Parameter ab, der gepackte Titel/Minuten/Sekunden/Frames (TMSF) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_TMSF_FRAME(
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

Gibt die Frames-Komponente der angegebenen TMSF-Informationen zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.

Das **MCI \_ TMSF- \_ Frame** -Makro wird wie folgt definiert:


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
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

 

 





