---
title: IWMDRMSecurity CheckCertForRevocation-Methode (Wmdrmsdk.h)
description: Die CheckCertForRevocation-Methode bestimmt, ob ein Zertifikat widerrufen wurde.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- CheckCertForRevocation-Methode windows Media Format
- CheckCertForRevocation-Methode windows Media Format, IWMDRMSecurity-Schnittstelle
- IWMDRMSecurity interface windows Media Format , CheckCertForRevocation method
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e090dfb655837ad2cf36cf45486488fde1440b499b73f16fdfbdaf2989532687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700786"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>IWMDRMSecurity::CheckCertForRevocation-Methode

Die **CheckCertForRevocation-Methode** bestimmt, ob ein Zertifikat widerrufen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rguidRevocationList* \[ In\]
</dt> <dd>

GUID, die die zu verwendende Sperrliste identifiziert. Legen Sie auf einen der Werte in der folgenden Tabelle fest.



| GUID-Konstante                 | Beschreibung                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| WMDRM \_ \_ REVOCATIONTYPE-APP    | Gibt die Sperrliste des Anwendungszertifikats an.                                     |
| WMDRM \_ \_ REVOCATIONTYPE-GERÄT | Gibt die Gerätezertifikatsperrliste an.                                          |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Gibt die Zertifikatsperrliste microsoft Windows Media DRM für Netzwerkgeräte an. |



 

</dd> <dt>

*pbCert* \[ In\]
</dt> <dd>

Puffer mit dem zu suchenden Zertifikat.

</dd> <dt>

*cbCert* \[ In\]
</dt> <dd>

Größe des Puffers *pbCert* in Bytes.

</dd> <dt>

*fRevoked* \[ out\]
</dt> <dd>

Gibt bei der Ausgabe an, ob das Zertifikat in der Sperrliste vorhanden ist.

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

[**IWMDRMSecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





