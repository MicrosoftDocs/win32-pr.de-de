---
title: MpErrorMessageFormat-Funktion (MpClient.h)
description: Gibt eine formatierte Fehlermeldung basierend auf einem Fehlercode zurück.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Legacy-Windows-Umgebungsfeatures der MpErrorMessageFormat-Funktion
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
ms.openlocfilehash: 124bf9e2c5c2ecc18f286b99f0c3b93695abd3f6a40853fcc47de580edef5db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883507"
---
# <a name="mperrormessageformat-function"></a>MpErrorMessageFormat-Funktion

Gibt eine formatierte Fehlermeldung basierend auf einem Fehlercode zurück.

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

*hMpHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Behandeln Sie die Schnittstelle des Schadsoftwareschutz-Managers. Dieses Handle wird von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben.

</dd> <dt>

*hrError* \[ In\]
</dt> <dd>

Typ: **HRESULT**

Ein **HRESULT-basierter** Fehlercode.

</dd> <dt>

*pwszErrorDesc* \[ out\]
</dt> <dd>

Typ: **LPWSTR \***

Gibt eine formatierte Fehlermeldung basierend auf *hrError* zurück. Diese Zeichenfolge muss mit [**mpFreeMemory**](mpfreememory.md)freigegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **S \_ OK.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.**

## <a name="remarks"></a>Hinweise

Diese Funktion kann Systemfehlercodes zusätzlich zu bestimmten Fehlercodes formatieren, die von Funktionen zum Schutz vor Schadsoftware zurückgegeben werden. Die  HRESULT-Fehlercodes, die für Schadsoftwareschutzfunktionen spezifisch sind, verfügen über 0x50. Im Folgenden finden Sie eine Liste mit einer Teilmenge der spezifischen Fehlercodes für den Schadsoftwareschutz, die von verschiedenen Funktionen zum Schutz vor Schadsoftware zurückgegeben werden können. Mithilfe des Makros **HRESULT \_ FROM MP \_ \_ STATUS** können die folgenden Fehlercodes in **HRESULT** konvertiert werden. Eine Liste anderer möglicher Fehlercodes finden Sie unter Fehlercodes der [Antischadsoftware-Engine für Forefront Client Security.](https://support.microsoft.com/kb/939359)



| Fehlercode                              | BESCHREIBUNG                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| FEHLER \_ MP \_ NOENGINE                     | Es wird keine Engine in den Antischadsoftwaredienst geladen, um den angeforderten Vorgang auszuführen.                                              |
| FEHLER \_ MP \_ KEIN \_ ARBEITSSPEICHER                   | Bei der Antischadsoftware-Engine ist eine Situation ohne Arbeitsspeicher aufgetreten.                                                               |
| FEHLER \_ MP \_ REMOVE \_ FAILED               | Fehler beim Entfernen des Vorgangs für eine bestimmte Bedrohung.                                                                              |
| FEHLER \_ \_ BEI MP-QUARANTÄNEFEHLER \_           | Fehler beim Quarantänevorgang für eine bestimmte Bedrohung.                                                                          |
| FEHLER \_ \_ MP-BEDROHUNG \_ NICHT \_ GEFUNDEN           | Die spezifische Bedrohung ist im System nicht mehr vorhanden.                                                                         |
| FEHLER \_ MP REMOVE NICHT \_ \_ \_ UNTERSTÜTZT       | Der Entfernungsvorgang für eine bestimmte Bedrohung innerhalb des Containertyps wird nicht unterstützt.                                          |
| FEHLER \_ MP \_ REMOVE \_ IMMUTABLE \_ CONTAINER | Aufgrund der Engine-Richtlinie wird ein Entfernungsvorgang einer bestimmten Bedrohung innerhalb eines blockierten Containers nicht unterstützt. (E-Mail-Archive.) |
| FEHLER \_ MP \_ BADDB \_ OLDENGINE             | Die Signaturupdateanforderung hat eine ältere Engine oder Signaturdateien bereitgestellt.                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[Fehlercodes der Antischadsoftware-Engine für Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





