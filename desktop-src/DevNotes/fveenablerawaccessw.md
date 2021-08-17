---
description: Aktiviert oder deaktiviert das Lesen und Schreiben von Datenträgersektoren.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 050983663b782d40c330092919b8fc29060cbba057a16d147b80c6ea477cbf54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956089"
---
# <a name="fveenablerawaccessw-function"></a>FveEnableRawAccessW-Funktion

Aktiviert oder deaktiviert das Lesen und Schreiben von Datenträgersektoren.

## <a name="syntax"></a>Syntax


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VolumeName* \[ In\]
</dt> <dd>

Ein eindeutiger Bezeichner für das Datenträgervolumen.

</dd> <dt>

*Aktiviert* \[ In\]
</dt> <dd>

True **gibt an,** dass der Zugriff auf das rohe Volume möglich ist. False **gibt an,** dass kein Zugriff auf das rohe Volume zulässig ist. Wenn roher Zugriff bereits aktiviert wurde, dieser Wert jedoch **FALSE ist,** wird das Volume erneut bereitgestellt und erneut aktiviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                           | Beschreibung                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                           | Die Funktion war erfolgreich.<br/>                                            |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Aktiviert ist **FALSE,** und das Volume war noch nicht im Rohdatenzugriffsmodus.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | Das Volume kann nicht gesperrt werden.<br/>                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




