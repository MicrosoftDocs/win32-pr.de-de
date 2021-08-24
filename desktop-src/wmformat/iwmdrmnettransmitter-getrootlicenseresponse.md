---
title: IWMDRMNetTransmitter GetRootLicenseResponse-Methode (Wmdrmsdk.h)
description: Die GetRootLicenseResponse-Methode generiert eine Antwortnachricht zur Stammlizenz.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- GetRootLicenseResponse-Methode windows Media Format
- GetRootLicenseResponse-Methode windows Media Format , IWMDRMNetTransmitter-Schnittstelle
- IWMDRMNetTransmitter-Schnittstelle windows Media Format , GetRootLicenseResponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89389163a9eae66a0dcda14dd6b9699d3db9650140cceac6498b2ab77a4e44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707930"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>IWMDRMNetTransmitter::GetRootLicenseResponse-Methode

Die **GetRootLicenseResponse-Methode** generiert eine Antwortnachricht zur Stammlizenz.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrKID* \[ In\]
</dt> <dd>

Base64-codierter Schlüsselbezeichner, der für die neue Stammlizenz verwendet werden soll. Der Schlüsselbezeichner sollte ein zufällig generierter GUID-Wert sein.

</dd> <dt>

*ppbLicenseResponse* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Adresse der generierten Lizenzantwort empfängt. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie **CoTaskMemFree** aufrufen.

</dd> <dt>

*pwLicenseResponse* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Lizenzantwort in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ \_ DRM- WIES ZU \_ \_ KLEIN**</dt> </dl> | Eine aktualisierte Inhaltssperrliste ist erforderlich.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Die generierte Stammlizenz wird mithilfe der Informationen aus den Lizenzaufforderungsdaten erstellt, die für die Schnittstelle verarbeitet werden, indem [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)aufgerufen wird.

Die Stammlizenz wird bei der Generierung von Blattlizenzen verwendet, die durch Aufrufen der [**GetLeafLicenseResponse-Methode**](iwmdrmnettransmitter-getleaflicenseresponse.md) erreicht wird. Die **IWMDRMNetTransmitter-Schnittstelle** verwaltet eine Kopie der Stammlizenz für diese Verwendung.

Die Stammlizenz, die durch Aufrufen dieser Methode erstellt wurde, verfügt über keine Richtlinien und ist so konfiguriert, dass sie nicht auf dem empfangenden Gerät beibehalten werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMNetTransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





