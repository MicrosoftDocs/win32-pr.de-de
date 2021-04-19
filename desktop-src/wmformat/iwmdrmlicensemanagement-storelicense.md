---
title: "\"Iwmdrmlicenabmanagement\" (storelicense-Methode) (wmdrmsdk. h)"
description: Die storelicense-Methode enthält eine Lizenz, die außerhalb des lokalen DRM-Subsystems im lokalen Lizenz Speicher generiert wurde.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Storelicense-Methode Windows Media-Format
- Storelicense-Methode Windows Media-Format, iwmdrmlicensmanagement-Schnittstelle
- Iwmdrmlicenabmanagement-Schnittstelle Windows Media-Format, storelicense-Methode
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
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369979"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>Iwmdrmlicenabmanagement:: storelicense-Methode

Die **storelicense** -Methode enthält eine Lizenz, die außerhalb des lokalen DRM-Subsystems im lokalen Lizenz Speicher generiert wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstraulicenseresponse* \[ in\]
</dt> <dd>

Lizenz Antwort Zeichenfolge, die decodiert und dem lokalen Lizenz Speicher hinzugefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode können Sie XMR-Lizenzen hinzufügen, die Sie im lokalen Lizenz Speicher erstellt haben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





