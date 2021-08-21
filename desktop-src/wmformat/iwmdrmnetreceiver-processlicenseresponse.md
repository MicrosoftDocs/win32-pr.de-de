---
title: IWMDRMNetReceiver ProcessLicenseResponse-Methode (Wmdrmsdk.h)
description: Die ProcessLicenseResponse-Methode verarbeitet die Lizenzantwort, die vom Sender als Antwort auf eine Lizenzforderung gesendet wird.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- 'ProcessLicenseResponse-Methode : Windows Media Format'
- ProcessLicenseResponse-Methode windows Media Format, IWMDRMNetReceiver-Schnittstelle
- IWMDRMNetReceiver-Schnittstelle Windows Media Format , ProcessLicenseResponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7ba84c7bf58091bb17500b0d35390062710a79a9a32b939ac8b9517cbcfaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700824"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a>IWMDRMNetReceiver::P rocessLicenseResponse-Methode

Die **ProcessLicenseResponse-Methode** verarbeitet die Lizenzantwort, die vom Sender als Antwort auf eine Lizenzforderung gesendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbLicenseResponse* \[ In\]
</dt> <dd>

Vom Sender empfangene Lizenzantwort.

</dd> <dt>

*cbLicenseResponse* \[ In\]
</dt> <dd>

Größe der Antwort in Bytes.

</dd> <dt>

*ppbWMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Adresse der internen Lizenzdarstellung für die Lizenz empfängt, die in der Lizenzantwortnachricht enthalten ist. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher durch Aufrufen von **CoTaskMemFree frei geben.** Dieser Parameter kann auf NULL festgelegt **werden,** wenn die Lizenzdarstellung nicht erforderlich ist.

</dd> <dt>

*–WMDRMNetLicenseRepresentation* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Lizenzdarstellung empfängt. Muss auf NULL festgelegt **werden,** *wenn ppbWMDRMNetLicenseRepresentation* **NULL ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ \_ DRM:NS: ZU \_ \_ KLEIN**</dt> </dl> | Eine aktualisierte Inhaltssperrliste ist erforderlich.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Die mit dieser Methode verarbeitete Lizenzantwort muss der letzten Lizenzausforderung entsprechen, die auf dem Clientcomputer generiert wurde.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMNetReceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetLicenseC wiege**](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





