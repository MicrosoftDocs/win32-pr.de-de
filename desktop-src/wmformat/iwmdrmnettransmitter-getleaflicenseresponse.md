---
title: IWMDRMNetTransmitter GetLeafLicenseResponse-Methode (Wmdrmsdk.h)
description: Die GetLeafLicenseResponse-Methode generiert eine Blattlizenzantwortnachricht.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- GetLeafLicenseResponse-Methode windows Media Format
- GetLeafLicenseResponse-Methode Windows Media Format, IWMDRMNetTransmitter-Schnittstelle
- IWMDRMNetTransmitter-Schnittstelle Windows Media Format , GetLeafLicenseResponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aff470341c3227782d0d34cbdd2ca2a4a51a4cb1b6214b81ea2ea9a384b29ee2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084830"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>IWMDRMNetTransmitter::GetLeafLicenseResponse-Methode

Die **GetLeafLicenseResponse-Methode** generiert eine Blattlizenzantwortnachricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrKID* \[ In\]
</dt> <dd>

Base64-codierter Schlüsselbezeichner, der für die neue Blattlizenz verwendet werden soll. Der Schlüsselbezeichner sollte ein zufällig generierter GUID-Wert sein.

</dd> <dt>

*pPolicy* \[ In\]
</dt> <dd>

Zeiger auf die [**WMDRMNET \_ POLICY-Struktur,**](wmdrmnet-policy.md) die die Richtlinie definiert, die für die Blattlizenz verwendet werden soll.

</dd> <dt>

*ppIWMDRMEncrypt* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**IWMDRMEncrypt-Schnittstelle**](iwmdrmencrypt.md) empfängt, die zum Verschlüsseln von Daten für die neue Blattlizenz verwendet werden kann.

</dd> <dt>

*ppbLicenseResponse* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Adresse der generierten Lizenzantwort empfängt. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher durch Aufrufen von **CoTaskMemFree frei geben.**

</dd> <dt>

*alphabetLicenseResponse* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Lizenzantwort in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ \_ DRM:NS: ZU \_ \_ KLEIN**</dt> </dl> | Eine aktualisierte Inhaltssperrliste ist erforderlich.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMNetTransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





