---
title: Iwmdrmdevice-setmeterresponse-Methode
description: Die setmeterresponse-Methode legt die Messungs Antwort fest.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Setmeterresponse-Methode (Windows Media Device Manager)
- Setmeterresponse-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, setmeterresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364677"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>Iwmdrmdevice:: setmeterresponse-Methode

Die **setmeterresponse** -Methode legt die Messungs Antwort fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbmeterantwort* \[ in\]
</dt> <dd>

Die festzulegende Messungs Antwort.

</dd> <dt>

*cbmeter Response* \[ in\]
</dt> <dd>

Größe der Messungs Antwort in Bytes.

</dd> <dt>

*pdwflags* \[ vorgenommen\]
</dt> <dd>

Antwortflags. Bei diesem Wert muss es sich um eines der folgenden Flags handeln.



| Flag                            | Beschreibung              |
|---------------------------------|--------------------------|
| WMDRM- \_ Zähler für \_ \_ alle Zähler     | Alle Meter Antworten.     |
| WMDRM- \_ Messgeräte \_ Antwort \_ partiell | Teil Messungs Antworten. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmddrmsp. idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmdevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





