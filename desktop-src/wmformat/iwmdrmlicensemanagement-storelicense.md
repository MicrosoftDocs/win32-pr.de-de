---
title: IWMDRMLicenseManagement StoreLicense-Methode (Wmdrmsdk.h)
description: Die StoreLicense-Methode enthält eine Lizenz, die außerhalb des lokalen DRM-Subsystems im lokalen Lizenzspeicher generiert wurde.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- 'StoreLicense-Methode : Windows-Medienformat'
- StoreLicense-Methode windows Media Format, IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle Windows Media Format , StoreLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c509fdbc89acfd2d31ad5ead7ce63cd7f3b501b304d82240475c845c013e03b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655048"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>IWMDRMLicenseManagement::StoreLicense-Methode

Die **StoreLicense-Methode** enthält eine Lizenz, die außerhalb des lokalen DRM-Subsystems im lokalen Lizenzspeicher generiert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrLicenseResponse* \[ In\]
</dt> <dd>

Lizenzantwortzeichenfolge, die decodiert und dem lokalen Lizenzspeicher hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Mit dieser Methode können Sie dem lokalen Lizenzspeicher XMR-Lizenzen hinzufügen, die Sie erstellt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





