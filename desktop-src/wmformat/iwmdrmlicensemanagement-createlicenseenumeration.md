---
title: Iwmdrmlicencmanagement | atelicenabenumeration-Methode (wmdrmsdk. h)
description: Die Methode "samatelicenseenumeration" erstellt ein Lizenz-Enumeratorobjekt, mit dem Sie Informationen zu Lizenzen im lokalen Lizenz Speicher erhalten können.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Windows Media-Format für die Methode "samatelicenabenumeration"
- Methode "kreatelicenabenumeration" Windows Media-Format, iwmdrmlicensitzungsschnittstelle
- Iwmdrmlicencmanagement-Schnittstelle Windows Media-Format, Methode "kreatelicenabenumeration"
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364586"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>Iwmdrmlicenaberation-Methode

Die Methode " **samatelicenseenumeration** " erstellt ein Lizenz-Enumeratorobjekt, mit dem Sie Informationen zu Lizenzen im lokalen Lizenz Speicher erhalten können.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plicenabfilter* \[ in\]
</dt> <dd>

Zeiger auf eine [**WMDRM- \_ Lizenz \_ Filter**](wmdrm-license-filter.md) Struktur, die die Filter Parameter für die Liste der Lizenzen im Enumerator enthält.

</dd> <dt>

*Pendler* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, der die Adresse der [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle des neu erstellten License-Enumeratorobjekts empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt> </dl> | Es wird eine aktualisierte Inhalts Sperr Liste benötigt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Auflisten von Lizenzen im lokalen Lizenz Speicher**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





