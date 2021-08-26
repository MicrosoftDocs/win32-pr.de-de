---
title: IWMDRMLicenseManagement CreateLicenseEnumeration-Methode (Wmdrmsdk.h)
description: Die CreateLicenseEnumeration-Methode erstellt ein Lizenzenumeratorobjekt, mit dem Sie Informationen zu Lizenzen im lokalen Lizenzspeicher erhalten können.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- CreateLicenseEnumeration-Methode windows Media Format
- CreateLicenseEnumeration-Methode windows Media Format, IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , CreateLicenseEnumeration-Methode
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
ms.openlocfilehash: 2e442870961735d09c786a21ed1ea8be765e8f0c59b3f760278be9316daa0bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881080"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a>IWMDRMLicenseManagement::CreateLicenseEnumeration-Methode

Die **CreateLicenseEnumeration-Methode** erstellt ein Lizenzenumeratorobjekt, mit dem Sie Informationen zu Lizenzen im lokalen Lizenzspeicher erhalten können.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pLicenseFilter* \[ In\]
</dt> <dd>

Zeiger auf eine [**WMDRM LICENSE \_ \_ FILTER-Struktur,**](wmdrm-license-filter.md) die die Filterparameter für die Liste der Lizenzen im Enumerator enthält.

</dd> <dt>

*pEnumerator* \[ out\]
</dt> <dd>

Zeiger, der die Adresse der [**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md) des neu erstellten Lizenz-Enumeratorobjekts empfängt.

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
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Aufzählen von Lizenzen im lokalen Store**](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





