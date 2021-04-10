---
title: MCI_TMSF_SECOND-Makro (mciapi. h)
description: Das zweite MCI \_ TMSF- \_ Makro ruft die Sekunden Komponente von einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF) enthält.
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND Makro Windows Multimedia
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
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104007"
---
# <a name="mci_tmsf_second-macro"></a>Zweites MCI \_ TMSF- \_ Makro

Das **\_ \_ zweite MCI TMSF** -Makro ruft die Sekunden Komponente von einem Parameter ab, der gepackte Spuren/Minuten/Sekunden/Frames (TMSF) enthält.

## <a name="syntax"></a>Syntax


```C++
BYTE MCI_TMSF_SECOND(
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

Gibt die Sekunden Komponente der angegebenen TMSF-Informationen zurück.

## <a name="remarks"></a>Bemerkungen

Die Zeit im TMSF-Format wird als **DWORD** -Wert mit dem niedrigsten signifikanten Byte, das die Nachverfolgung enthält, dem nächst bedeutsamen Byte mit den Minuten, dem nächstniedrigsten Byte mit den Sekunden und dem signifikantesten Byte mit Frames ausgedrückt.

Das **\_ \_ zweite MCI TMSF** -Makro wird wie folgt definiert:


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
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

 

 





