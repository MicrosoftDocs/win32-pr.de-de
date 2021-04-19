---
title: Iwmdrmsecurity getrevocationdataversion-Methode (wmdrmsdk. h)
description: Die getrevocationdataversion-Methode ruft die Versionsnummer einer Zertifikat Sperr Liste im lokalen Speicher ab.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Getrevocationdataversion-Methode Windows Media-Format
- Getrevocationdataversion-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getrevocationdataversion-Methode
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
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356357"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a>Iwmdrmsecurity:: getrevocationdataversion-Methode

Die **getrevocationdataversion** -Methode ruft die Versionsnummer einer Zertifikat Sperr Liste im lokalen Speicher ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
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

*f \_ pdwcrlversion* \[ out\]
</dt> <dd>

Variable, die die Versionsnummer empfängt.

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

[**Getrevocationdata**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> <dt>

[**"Abtrevocationdata"**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





