---
title: IWMDRMLicenseManagement DeleteLicense-Methode (Wmdrmsdk.h)
description: Die DeleteLicense-Methode entfernt eine Lizenz aus dem temporären lokalen Lizenzspeicher.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- 'DeleteLicense-Methode : Windows-Medienformat'
- DeleteLicense-Methode windows Media Format, IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , DeleteLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977f7eaef1d6c8a505ce55d7d1683d7c9f4dabff5e59df7d8845773eefdff696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707940"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>IWMDRMLicenseManagement::D eleteLicense-Methode

Die **DeleteLicense-Methode** entfernt eine Lizenz aus dem temporären lokalen Lizenzspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrKID* \[ In\]
</dt> <dd>

Schlüssel-ID (KEY ID, KID) der zu löschenden Lizenz.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags für Die Option zum Löschen von Lizenzen. Legen Sie auf einen der Werte in der folgenden Tabelle fest.



| Wert                                    | Beschreibung                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDRM: \_ LIZENZ \_ SOFORT \_ LÖSCHEN      | Gibt an, dass die Lizenz sofort aus dem Speicher entfernt werden soll.                                                                                                                              |
| WMDRM \_ DELETE \_ LICENSE \_ MARK \_ FOR \_ PURGE | Gibt an, dass die Lizenz zum Löschen markiert, aber erst aus dem Speicher entfernt werden soll, wenn die [**CleanLicenseStore-Methode**](iwmdrmlicensemanagement-cleanlicensestore.md) aufgerufen wird. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                            | Beschreibung                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                    |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | Die angegebene Lizenz ist im Speicher nicht vorhanden.<br/> -ODER-<br/> Der Speicher wurde nicht gefunden.<br/> |



 

## <a name="remarks"></a>Hinweise

Um Lizenzen aus dem permanenten lokalen Lizenzspeicher zu löschen, müssen Sie die Lizenzsperrung verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





