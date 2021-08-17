---
title: IWMDRMLicense GetLicenseProperty-Methode (Wmdrmsdk.h)
description: Die GetLicenseProperty-Methode ruft eine Eigenschaft aus der aktuellen Lizenz ab.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- GetLicenseProperty-Methode windows Media Format
- GetLicenseProperty-Methode windows Media Format , IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle windows Media Format , GetLicenseProperty-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 167fc0aa050765700805b4339e68142fa5d1eb7fc99e010c7393095dd9aa5c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084840"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>IWMDRMLicense::GetLicenseProperty-Methode

Die **GetLicenseProperty-Methode** ruft eine Eigenschaft aus der aktuellen Lizenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* \[ In\]
</dt> <dd>

Name der abzurufende Eigenschaft. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest:



| Konstante                   | Beschreibung                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRMNet \_ Revocation | Verwenden Sie , um die Sperrliste für Windows Medien-DRM für Netzwerkgeräte für die aktuelle Lizenz abzurufen.                        |
| g \_ wszWMDRM \_ SAPLEVEL      | Verwenden Sie , um die SAP-Ebene (Secure Audio Path) abzurufen, die zum Wiedergeben von Inhalten erforderlich ist, die durch die aktuelle Lizenz abgedeckt sind.                |
| g \_ wszWMDRM \_ SAPRequired   | Verwenden Sie , um festzustellen, ob die aktuelle Lizenz erfordert, dass SAP zum Wiedergeben der Inhalte verwendet wird.                               |
| g \_ wszWMDRM \_ SOURCEID      | Verwenden Sie , um den Quellbezeichner für die aktuelle Lizenz abzurufen.                                                            |
| g \_ wszWMDRM \_ PRIORITY      | Verwenden Sie , um die Priorität der aktuellen Lizenz abzurufen. Lizenzen mit höherer Priorität werden vor Lizenzen mit niedrigerer Priorität angewendet. |
| g \_ wszWMDRM \_ UplinkID      | Verwenden Sie , um die Schlüssel-ID der Stammlizenz in der Lizenzkette abzurufen, zu der die aktuelle Lizenz gehört.                  |



 

</dd> <dt>

*ppropVariant* \[ out\]
</dt> <dd>

Empfängt den Eigenschaftswert.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





