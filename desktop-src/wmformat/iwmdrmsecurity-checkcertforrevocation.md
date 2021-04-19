---
title: Iwmdrmsecurity checkcertforwiderruf-Methode (wmdrmsdk. h)
description: Die checkcertforwiderruf-Methode bestimmt, ob ein Zertifikat gesperrt wurde.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Checkcertforwiderruf-Methode Windows Media-Format
- Checkcertforwiderruf-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, checkcertforwiderruf-Methode
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
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365958"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>Iwmdrmsecurity:: checkcertforwiderruf-Methode

Die **checkcertforwiderruf** -Methode bestimmt, ob ein Zertifikat gesperrt wurde.

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

*rguidrevocationlist* \[ in\]
</dt> <dd>

GUID, die die zu verwendende Sperr Liste identifiziert. Legen Sie auf einen der Werte in der folgenden Tabelle fest.



| GUID-Konstante                 | BESCHREIBUNG                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| WMDRM- \_ revocationtype- \_ App    | Gibt die Sperr Liste für das Anwendungs Zertifikat an.                                     |
| WMDRM- \_ revocationtype- \_ Gerät | Gibt die Zertifikat Sperr Liste für das Gerät an.                                          |
| WMDRM \_ revocationtype \_ Cardea | Gibt die Zertifikat Sperr Liste für Microsoft Windows Media DRM für Netzwerkgeräte an. |



 

</dd> <dt>

*pbcert* \[ in\]
</dt> <dd>

Puffer, der das zu überprüfen Zertifikat enthält.

</dd> <dt>

*cbcert* \[ in\]
</dt> <dd>

Größe des Puffers *pbcert*(in Bytes).

</dd> <dt>

*frei.* \[ vorgenommen\]
</dt> <dd>

Gibt bei Ausgabe an, ob das Zertifikat in der Sperr Liste vorhanden ist.

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

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





