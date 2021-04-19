---
description: Wird von Anwendungen verwendet, um dem Benutzer ein Dialogfeld für das Gerät anzuzeigen.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Devicedialog-Funktion (wiadevd. h)
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
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349429"
---
# <a name="devicedialog-function"></a>Devicedialog-Funktion

Wird von Anwendungen verwendet, um dem Benutzer ein Dialogfeld für das Gerät anzuzeigen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevicedialogdata* \[ in\]
</dt> <dd>

Typ: **pdevicedialogdata**

Die [**devicedialogdata**](-wia-devicedialogdata.md) , die zum Erstellen des Dialog Felds für das Gerät verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Devicedialogdata**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




