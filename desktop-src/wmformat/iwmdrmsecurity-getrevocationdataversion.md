---
title: IWMDRMSecurity GetRevocationDataVersion-Methode (Wmdrmsdk.h)
description: Die GetRevocationDataVersion-Methode ruft die Versionsnummer einer Zertifikatsperrliste im lokalen Speicher ab.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- GetRevocationDataVersion-Methode windows Media Format
- GetRevocationDataVersion-Methode windows Media Format, IWMDRMSecurity-Schnittstelle
- IWMDRMSecurity interface windows Media Format , GetRevocationDataVersion method
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d139b2daf3f3bc6ad78beaa50e19c0141aecd5e8bedac2dd20582fb1536d9b74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930780"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>IWMDRMSecurity::GetRevocationDataVersion-Methode

Die **GetRevocationDataVersion-Methode** ruft die Versionsnummer einer Zertifikatsperrliste im lokalen Speicher ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*f \_ guidRevocationType* \[ in\]
</dt> <dd>

GUID, die den Typ der Sperrliste an gibt. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.



| GUID-Konstante                 | Beschreibung                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM \_ \_ REVOCATIONTYPE-APP    | Gibt die Sperrliste des Anwendungszertifikats an.                           |
| WMDRM \_ \_ REVOCATIONTYPE-GERÄT | Gibt die Gerätezertifikatsperrliste an.                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Gibt die zertifikatssperrliste Windows Medien-DRM für Netzwerkgeräte an. |



 

</dd> <dt>

*f \_ pdwCRLVersion* \[ out\]
</dt> <dd>

Variable, die die Versionsnummer empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Automatisiertes Widerrufen und Erneuern von Komponenten**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**IWMDRMSecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





