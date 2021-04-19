---
title: Iwmdrmlicensequery-Methode für die Methode "-Methode" (wmdrmsdk. h)
description: Die setactionaccesswedqueryparams-Methode legt Umgebungs spezifische Informationen für genauere Abfrageergebnisse fest, wenn die queryAction Allowed-Methode verwendet wird.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- "\"\"-Methode für die \"\"-Methode \"\" der Methode \"\" in Windows Media"
- Die Methode "" der Klasse "" ist ein Windows Media-Format, die iwmdrmlicensequery-Schnittstelle
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format, Methode "Methode"
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359262"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a>Iwmdrmlicensequery:: ""-Methode

Die **setactionaccesswedqueryparams** -Methode legt Umgebungs spezifische Informationen für genauere Abfrageergebnisse fest, wenn die [**queryAction Allowed**](iwmdrmlicensequery-queryactionallowed.md) -Methode verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fsmf* \[ in\]
</dt> <dd>

Gibt an, ob der Inhalt mithilfe der Objekte des Microsoft Media Foundation SDK gerendert wird. **False** gibt das Rendering durch die Objekte des Windows Media Format SDK an. Dieser Parameter ist optional.

</dd> <dt>

*dwappberclevel* \[ in\]
</dt> <dd>

Sicherheitsstufe der Abfrageanwendung. Dieser Wert ist nur wichtig, wenn die Objekte des Windows Media Format SDK verwendet werden. in diesem Fall sollte " *fsmf* " auf " **false**" festgelegt werden. Dieser Parameter ist optional.

</dd> <dt>

" *shasserialnumber* \[ " in\]
</dt> <dd>

Gibt an, ob das Zielgerät für einen Kopiervorgang über eine Seriennummer verfügt. Dieser Parameter ist optional und gilt nur für Abfragen für Kopiervorgänge.

</dd> <dt>

*bstraude vicecert* \[ in\]
</dt> <dd>

Gerätezertifikat des Zielgeräts, wenn Windows Media DRM für tragbare Geräte verwendet wird. Dieser Parameter ist optional und gilt nur für Abfragen für Kopiervorgänge.

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

[**Iwmdrmlicensequery-Schnittstelle**](iwmdrmlicensequery.md)
</dt> <dt>

[**Abfragen ausführlicher Rechte Informationen**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





