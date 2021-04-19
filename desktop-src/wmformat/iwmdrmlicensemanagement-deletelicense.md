---
title: Iwmdrmlicenabmanagement-Methode "Delta-eLicense" (wmdrmsdk. h)
description: Mit der Methode "Delta-eLicense" wird eine Lizenz aus dem temporären lokalen Lizenz Speicher entfernt.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Delta-eLicense-Methode, Windows Media-Format
- Delta-eLicense-Methode, Windows Media-Format, iwmdrmlicencmanagement-Schnittstelle
- Iwmdrmlicencmanagement-Schnittstelle Windows Media-Format, Delta eLicense-Methode
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
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373816"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a>Iwmdrmlicensmanagement::D eletelicense-Methode

Mit der Methode " **Delta-eLicense** " wird eine Lizenz aus dem temporären lokalen Lizenz Speicher entfernt.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinkid* \[ in\]
</dt> <dd>

Die Schlüssel-ID (Kid) der zu löschenden Lizenz.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Options Flags zum Löschen von Lizenzen. Legen Sie auf einen der Werte in der folgenden Tabelle fest.



| Wert                                    | BESCHREIBUNG                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ - \_ Lizenz \_ sofort löschen      | Gibt an, dass die Lizenz sofort aus dem Speicher entfernt werden soll.                                                                                                                              |
| WMDRM \_ - \_ Lizenz \_ Markierung \_ zum \_ Löschen löschen | Gibt an, dass die Lizenz zum Löschen markiert werden soll, jedoch nicht aus dem Speicher entfernt werden soll, bis die [**cleanlicencstore**](iwmdrmlicensemanagement-cleanlicensestore.md) -Methode aufgerufen wird. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                            | Beschreibung                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                                                                    |
| <dl> <dt>**DRM- \_ E \_ licensenotfound**</dt> </dl> | Die angegebene Lizenz ist nicht im Speicher vorhanden.<br/> -ODER-<br/> Der Speicher wurde nicht gefunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Zum Löschen von Lizenzen aus dem permanenten lokalen Lizenz Speicher müssen Sie die Lizenz Sperrung verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





