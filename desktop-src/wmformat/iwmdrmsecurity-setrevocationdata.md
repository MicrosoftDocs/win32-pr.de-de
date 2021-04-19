---
title: Iwmdrmsecurity-Methode "* trevocationdata" (wmdrmsdk. h)
description: Die setrevocationdata-Methode legt eine Zertifikat Sperr Liste im lokalen Speicher fest.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- "\"Strevocationdata\"-Methode, Windows Media-Format"
- "\"Ttrevocationdata\"-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle"
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, Methode "Methode"
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369978"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a>Iwmdrmsecurity:: abtrevocationdata-Methode

Die **setrevocationdata** -Methode legt eine Zertifikat Sperr Liste im lokalen Speicher fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*f \_ guidrevocationtype* \[ in\]
</dt> <dd>

GUID, die den Typ der Sperr Liste angibt. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.



| GUID-Konstante                 | BESCHREIBUNG                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| WMDRM- \_ revocationtype- \_ App    | Gibt die Sperr Liste für das Anwendungs Zertifikat an.                           |
| WMDRM- \_ revocationtype- \_ Gerät | Gibt die Zertifikat Sperr Liste für das Gerät an.                                |
| WMDRM \_ revocationtype \_ Cardea | Gibt die Zertifikat Sperr Liste für Windows Media DRM für Netzwerkgeräte an. |



 

</dd> <dt>

*f \_ pbcrl* \[ in\]
</dt> <dd>

Puffer, der die Zertifikat Sperr Liste enthält.

</dd> <dt>

*f \_ cbcrl* \[ in\]
</dt> <dd>

Größe des Puffers in Bytes.

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

[**Getrevocationdata**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Getrevocationdataversion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





