---
title: Iwmdrmsecurity getrevocationdata-Methode (wmdrmsdk. h)
description: Die getrevocationdata-Methode ruft eine Zertifikat Sperr Liste aus dem lokalen Speicher ab.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Getrevocationdata-Methode, Windows Media-Format
- Getrevocationdata-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getrevocationdata-Methode
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
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357977"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>Iwmdrmsecurity:: getrevocationdata-Methode

Die **getrevocationdata** -Methode ruft eine Zertifikat Sperr Liste aus dem lokalen Speicher ab.

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

*f \_ guidrevocationtype* \[ in\]
</dt> <dd>

GUID, die den Typ der abzurufenden Sperr Liste identifiziert. Verwenden Sie eine der-Konstanten in der folgenden Tabelle.



| GUID-Konstante                 | BESCHREIBUNG                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM- \_ revocationtype- \_ App    | Gibt die Sperr Liste für das Anwendungs Zertifikat an.                           |
| WMDRM- \_ revocationtype- \_ Gerät | Gibt die Zertifikat Sperr Liste für das Gerät an.                                |
| WMDRM \_ revocationtype \_ Cardea | Gibt die Zertifikat Sperr Liste für Windows Media DRM für Netzwerkgeräte an. |



 

</dd> <dt>

*f \_ pbcrl* \[ out\]
</dt> <dd>

Puffer, der die Sperr Liste empfängt. Auf **null** festgelegt, um die erforderliche Puffergröße zu erhalten.

</dd> <dt>

*f \_ pcbcrl* \[ in, out\]
</dt> <dd>

Größe des Puffers in Byte. Wenn *f \_ pbcrl* **null** ist, wird dieser Wert auf die erforderliche Puffergröße bei der Ausgabe festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Automatisierte Sperrung und Erneuerung von Komponenten**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Getrevocationdataversion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> <dt>

[**"Abtrevocationdata"**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





