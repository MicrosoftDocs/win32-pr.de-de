---
title: IWMDRMLicenseManagement CreateLicenseRevocationCrelige-Methode (Wmdrmsdk.h)
description: Die CreateLicenseRevocationCantenge-Methode generiert eine Lizenzsperrungs-Challenge.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- CreateLicenseRevocationCrelige-Methode windows Media Format
- CreateLicenseRevocationChallenge-Methode windows Media Format, IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , CreateLicenseRevocationCrelige-Methode
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
ms.openlocfilehash: 851233229d7dde113cf21cfb38419067679843b34ae59ece0e32e326c2a91c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846953"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a>IWMDRMLicenseManagement::CreateLicenseRevocationChallenge-Methode

Die **CreateLicenseRevocationCantenge-Methode** generiert eine Lizenzsperrungs-Challenge.

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

*pbMachineID* \[ In\]
</dt> <dd>

Bezeichner des vom Benutzer angegebenen Computers. Dieser Wert wird zum Abfragen einer Lizenz auf dem Server verwendet und muss dem format entsprechen, das der Lizenzserver verwendet.

</dd> <dt>

*cbMachineID* \[ In\]
</dt> <dd>

Größe des Computerbezeichners in Bytes.

</dd> <dt>

*pbChallenge* \[ In\]
</dt> <dd>

Vom Benutzer angegebene Herausforderungsdaten. Diese Daten werden zusätzlich zur Computer-ID verwendet, um den Lizenzserver nach widerrufenen Lizenzen zu fragen.

</dd> <dt>

*cbChallenge* \[ In\]
</dt> <dd>

Größe der Herausforderungsdaten in Bytes.

</dd> <dt>

*ppbCppegeOutput* \[ out\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der Ausgabe der Herausforderung empfängt. Dieser Puffer ist die Daten, die an den Lizenzsperrdienst gesendet werden. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher durch Aufrufen von **CoTaskMemFree frei geben.**

</dd> <dt>

*beiChallengeOutput* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Größe der zugeordneten Ausgabedaten der Herausforderung in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





