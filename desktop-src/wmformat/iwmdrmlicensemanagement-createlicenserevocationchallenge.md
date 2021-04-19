---
title: Iwmdrmlicencmanagement | atelicenserevocationchallenge-Methode (wmdrmsdk. h)
description: Die Methode "samatelicenserevocationchallenge" generiert eine Lizenz Sperr Aufforderung.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Methode "samatelicenserevocationchallenge" Windows Media Format
- Methode "samatelicenserevocationchallenge" Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicencmanagement-Schnittstelle Windows Media-Format, Methode "kreatelicenserevocationchallenge"
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361498"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>Iwmdrmlicenabmanagement:: samatelicenserevocationchallenge-Methode

Die Methode " **samatelicenserevocationchallenge** " generiert eine Lizenz Sperr Aufforderung.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbmachineid* \[ in\]
</dt> <dd>

Vom Benutzer angegebener Computer Bezeichner. Dieser Wert wird verwendet, um eine Lizenz auf dem Server abzufragen, und muss dem vom Lizenzserver verwendeten Format entsprechen.

</dd> <dt>

*cbmachineid* \[ in\]
</dt> <dd>

Größe (in Bytes) des Computer Bezeichners.

</dd> <dt>

*pbchallenge* \[ in\]
</dt> <dd>

Vom Benutzer angegebene Abfrage Daten. Diese Daten werden zusätzlich zum Computer Bezeichner verwendet, um den Lizenzserver abzufragen, damit Lizenzen widerrufen werden.

</dd> <dt>

*cbchallenge* \[ in\]
</dt> <dd>

Größe der Abfrage Daten in Bytes.

</dd> <dt>

*ppbherausfordergeoutput* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der Challenge-Ausgabe empfängt. Dieser Puffer stellt die Daten dar, die an den Lizenz Sperr Dienst gesendet werden. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.

</dd> <dt>

*pcbherausfordergeoutput* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Größe der zugeordneten Challenge-Ausgabedaten in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





