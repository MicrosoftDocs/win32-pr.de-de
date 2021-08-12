---
description: Wird von Anwendungen verwendet, um dem Benutzer ein Gerätedialogfeld anzuzeigen.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: DeviceDialog-Funktion (Wiadevd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: de8a3d36472d51c24a2c007ad7be0be371a0b5d8bb39e75f457e204250e8f53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441678"
---
# <a name="devicedialog-function"></a>DeviceDialog-Funktion

Wird von Anwendungen verwendet, um dem Benutzer ein Gerätedialogfeld anzuzeigen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDeviceDialogData* \[ In\]
</dt> <dd>

Typ: **PDEVICEDIALOGDATA**

Der [**DEVICEDIALOGDATA-Wert,**](-wia-devicedialogdata.md) der zum Erstellen des Gerätedialogfelds verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wiadevd.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




