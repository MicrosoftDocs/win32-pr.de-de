---
title: Iwmdrmlicense GetLicense-Methode (wmdrmsdk. h)
description: Die GetLicense-Methode ruft die Lizenz als XML-oder XMR-Daten ab.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- GetLicense-Methode Windows Media-Format
- GetLicense-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, GetLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361937"
---
# <a name="iwmdrmlicensegetlicense-method"></a>Iwmdrmlicense:: GetLicense-Methode

Die **GetLicense** -Methode ruft die Lizenz als XML-oder XMR-Daten ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppblicense* \[ vorgenommen\]
</dt> <dd>

Empfängt die Lizenz.

</dd> <dt>

*pcblicense* \[ vorgenommen\]
</dt> <dd>

Empfängt die Größe der Lizenz.

</dd> <dt>

*pdwlicensertype* \[ vorgenommen\]
</dt> <dd>

Empfängt den Typ der zurückgegebenen Lizenz. Dieser Wert wird auf eine der Konstanten in der folgenden Tabelle festgelegt.



| Konstante                  | BESCHREIBUNG                            |
|---------------------------|----------------------------------------|
| WMDRM \_ - \_ Lizenztyp- \_ XML | Die abgerufene Lizenz wird als XML formatiert. |
| WMDRM \_ - \_ Lizenztyp \_ XMR | Die abgerufene Lizenz ist als XMR formatiert. |



 

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

[**Getliceneinproperty**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





