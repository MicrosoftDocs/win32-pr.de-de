---
title: IWMDRMSecurity GetRevocationData-Methode (Wmdrmsdk.h)
description: Die GetRevocationData-Methode ruft eine Zertifikatsperrliste aus dem lokalen Speicher ab.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- GetRevocationData-Methode windows Media Format
- GetRevocationData-Methode windows Media Format , IWMDRMSecurity-Schnittstelle
- IWMDRMSecurity-Schnittstelle windows Media Format , GetRevocationData-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5035bc94051c61baaef7bcf474b4d6ebb4413b549dfff038bae7105f32d087b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808480"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>IWMDRMSecurity::GetRevocationData-Methode

Die **GetRevocationData-Methode** ruft eine Zertifikatsperrliste aus dem lokalen Speicher ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*f \_ guidRevocationType* \[ in\]
</dt> <dd>

GUID, die den Typ der abzurufenden Sperrliste identifiziert. Verwenden Sie eine der Konstanten in der folgenden Tabelle.



| GUID-Konstante                 | Beschreibung                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM \_ \_ REVOCATIONTYPE-APP    | Gibt die Sperrliste des Anwendungszertifikats an.                           |
| WMDRM \_ REVOCATIONTYPE \_ DEVICE | Gibt die Sperrliste des Gerätezertifikats an.                                |
| WMDRM \_ REVOCATIONTYPE \_ CARDEA | Gibt die Zertifikatsperrliste Windows Medien-DRM für Netzwerkgeräte an. |



 

</dd> <dt>

*f \_ pbCRL* \[ out\]
</dt> <dd>

Puffer, der die Sperrliste empfängt. Legen Sie auf **NULL** fest, um die erforderliche Puffergröße abzurufen.

</dd> <dt>

*f \_ lpCRL* \[ in, out\]
</dt> <dd>

Größe des Puffers in Byte. Wenn *f \_ pbCRL* **NULL** ist, wird dieser Wert bei der Ausgabe auf die erforderliche Puffergröße festgelegt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Automatisierte Komponentensperrung und -verlängerung**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**IWMDRMSecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





