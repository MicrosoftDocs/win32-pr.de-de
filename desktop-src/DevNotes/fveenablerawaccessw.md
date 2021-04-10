---
description: Aktiviert oder deaktiviert das Lesen und Schreiben von Datenträger Sektoren.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: Funktion "sveenablerawaccessw"
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
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860903"
---
# <a name="fveenablerawaccessw-function"></a>Funktion "sveenablerawaccessw"

Aktiviert oder deaktiviert das Lesen und Schreiben von Datenträger Sektoren.

## <a name="syntax"></a>Syntax


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Volumename* \[ in\]
</dt> <dd>

Ein eindeutiger Bezeichner für das Datenträger Volume.

</dd> <dt>

*Aktiviert* \[ in\]
</dt> <dd>

Wenn der Wert **true** ist, wird der Zugriff auf das rohvolume ermöglicht. Wenn der Wert **false** ist, ist kein Zugriff auf das rohvolume zulässig. Wenn der rohzugriff bereits aktiviert wurde, dieser Wert jedoch **false** ist, wird das Volume erneut bereitgestellt und erneut überprüft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen der folgenden Codes oder einen anderen Fehlercode zurück, wenn ein Fehler auftritt.



| Rückgabecode/-wert                                                                                                                                                           | BESCHREIBUNG                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                           | Die Funktion war erfolgreich.<br/>                                            |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Aktiviert ist **false** , und das Volume war nicht bereits im RAW-Zugriffsmodus.<br/> |
| <dl> <dt>**E \_ AccessDenied**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | Das Volume kann nicht gesperrt werden.<br/>                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




