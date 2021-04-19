---
title: Iwmdrmlicense getlicencproperty-Methode (wmdrmsdk. h)
description: Die getlicencproperty-Methode ruft eine Eigenschaft aus der aktuellen Lizenz ab.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Getlicentproperty-Methode, Windows Media-Format
- Getlicentproperty-Methode, Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getlicentproperty-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370591"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a>Iwmdrmlicense:: getlicencproperty-Methode

Die **getlicencproperty** -Methode ruft eine Eigenschaft aus der aktuellen Lizenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Der Name der abzurufenden Eigenschaft. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest:



| Konstante                   | BESCHREIBUNG                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| g \_ wszwmdrmnet-Sperrung \_ | Verwenden Sie, um die Sperr Liste für Windows Media DRM für Netzwerkgeräte für die aktuelle Lizenz zu erhalten.                        |
| g \_ wszwmdrm ( \_ saplevel)      | Verwenden Sie, um die SAP-Ebene (Secure audiopath) zu erhalten, die zur Wiedergabe von Inhalten erforderlich ist, die von der aktuellen                |
| g \_ wszwmdrm \_ saprequired   | Verwenden Sie, um zu überprüfen, ob für die aktuelle Lizenz SAP zum Wiedergeben des Inhalts erforderlich ist.                               |
| g \_ wszwmdrm \_ SourceID      | Verwenden Sie, um den Quell Bezeichner für die aktuelle Lizenz zu erhalten.                                                            |
| g \_ wszwmdrm- \_ Priorität      | Verwenden Sie, um die Priorität der aktuellen Lizenz zu erhalten. Lizenzen mit höherer Priorität werden vor Lizenzen mit niedrigerer Priorität angewendet. |
| g \_ wszwmdrm \_ uplinkid      | Verwenden Sie, um die Schlüssel-ID der Stamm Lizenz in der Lizenz Kette zu erhalten, zu der die aktuelle Lizenz gehört.                  |



 

</dd> <dt>

*ppropvariant* \[ vorgenommen\]
</dt> <dd>

Empfängt den-Eigenschafts Wert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetLicense**](iwmdrmlicense-getlicense.md)
</dt> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





