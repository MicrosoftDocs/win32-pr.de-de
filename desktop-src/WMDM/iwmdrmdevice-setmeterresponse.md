---
title: IWMDRMDevice SetMeterResponse-Methode
description: Die SetMeterResponse-Methode legt die Messungsantwort fest.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- SetMeterResponse-Methode windows Media Geräte-Manager
- SetMeterResponse-Methode windows Media Geräte-Manager , IWMDRMDevice-Schnittstelle
- IWMDRMDevice interface windows Media Geräte-Manager , SetMeterResponse method
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
ms.openlocfilehash: b05941619d30ea067dc594e05b7b427ec5d825ef3e0c3c441cdfb3c723e94d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619570"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>IWMDRMDevice::SetMeterResponse-Methode

Die **SetMeterResponse-Methode** legt die Messungsantwort fest.

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

*pbMeterResponse* \[ In\]
</dt> <dd>

Die zu setzende Messungsantwort.

</dd> <dt>

*cbMeterResponse* \[ In\]
</dt> <dd>

Größe der Messungsantwort in Bytes.

</dd> <dt>

*pdwFlags* \[ out\]
</dt> <dd>

Antwortflags. Dieser Wert muss eines der folgenden Flags sein.



| Flag                            | Beschreibung              |
|---------------------------------|--------------------------|
| WMDRM \_ METER \_ RESPONSE \_ ALL     | Alle Zählerantworten.     |
| WMDRM \_ METER \_ RESPONSE \_ PARTIAL | Teilantworten der Verbrauchsmessung. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMDevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





