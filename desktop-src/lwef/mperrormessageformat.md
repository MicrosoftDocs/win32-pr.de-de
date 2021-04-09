---
title: Mperrormessageformat-Funktion (mpclient. h)
description: Gibt eine formatierte Fehlermeldung auf der Grundlage eines Fehlercodes zurück.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Mperrormessageformat-Funktion Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957045"
---
# <a name="mperrormessageformat-function"></a>Mperrormessageformat-Funktion

Gibt eine formatierte Fehlermeldung auf der Grundlage eines Fehlercodes zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.

</dd> <dt>

*hrError* \[ in\]
</dt> <dd>

Typ: **HRESULT**

Ein **HRESULT**-basierter Fehlercode.

</dd> <dt>

*pwszerrorde SC* \[ vorgenommen\]
</dt> <dd>

Typ: **LPWSTR \** _

Gibt eine formatierte Fehlermeldung zurück, die auf _hrError * basiert. Diese Zeichenfolge muss mithilfe von [**mpfrememory**](mpfreememory.md)freigegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist in der Lage, Systemfehler Codes zusätzlich zu bestimmten Fehlercodes zu formatieren, die von Malware Schutzfunktionen zurückgegeben werden. Die **HRESULT** -Fehlercodes, die für Malware Schutzfunktionen spezifisch sind, haben die Funktion 0x50. Im folgenden finden Sie eine Liste einer Teilmenge der Malware Schutz spezifischen Fehlercodes, die von verschiedenen Malware Schutzfunktionen zurückgegeben werden können. Die folgenden Fehlercodes können mit dem Makro **HRESULT \_ aus \_ MP- \_ Status** in **HRESULT** konvertiert werden. Eine Liste mit anderen möglichen Fehlercodes finden Sie auch in den [Fehlercodes für die Antischadsoftware-Engine von Forefront Client Security](https://support.microsoft.com/kb/939359) .



| Fehlercode                              | BESCHREIBUNG                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Fehler- \_ MP- \_ noengine                     | Es wurde keine Engine in den antischadsoftwaredienst geladen, um den angeforderten Vorgang auszuführen.                                              |
| Fehler \_ MP " \_ kein Arbeits \_ Speicher"                   | Die Antischadsoftware-Engine hat eine nicht genügend Arbeitsspeicher Situation gefunden.                                                               |
| Fehler beim \_ Entfernen des MP-Fehlers \_ \_               | Fehler beim Entfernungs Vorgang für eine bestimmte Bedrohung.                                                                              |
| Fehler bei \_ MP- \_ Quarantäne. \_           | Der Quarantäne Vorgang konnte für eine bestimmte Bedrohung nicht ausgeführt werden.                                                                          |
| Fehler- \_ MP- \_ Bedrohung \_ nicht \_ gefunden.           | Die spezifische Bedrohung ist im System nicht mehr vorhanden.                                                                         |
| Fehler \_ beim \_ Entfernen von MP \_ nicht \_ unterstützt       | Der Entfernungs Vorgang für eine bestimmte Bedrohung innerhalb des Container Typs wird nicht unterstützt.                                          |
| Fehler \_ MP \_ Entfernen eines \_ unveränderlichen \_ Containers | Aufgrund der Engine-Richtlinie wird ein Entfernungs Vorgang einer bestimmten Bedrohung in einem blockierten Container nicht unterstützt. (E-Mail-Archive.) |
| Fehler \_ MP \_ baddb \_ oldengine             | Die Signatur Aktualisierungs Anforderung hat eine ältere Engine oder Signatur Dateien bereitgestellt.                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mpfrememory**](mpfreememory.md)
</dt> <dt>

[**Mpmanageropen**](mpmanageropen.md)
</dt> <dt>

[Fehlercodes der Antischadsoftware-Engine für Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





