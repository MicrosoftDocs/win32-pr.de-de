---
title: Iwmdrmdevice (setsecureclockresponse-Methode)
description: Die setsecureclockresponse-Methode legt die Antwort auf die sichere Uhr fest.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Setsecureclockresponse-Methode, Windows Media Device Manager
- Setsecureclockresponse-Methode Windows Media Device Manager, iwmdrmdevice-Schnittstelle
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, setsecureclockresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365928"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>Iwmdrmdevice:: setsecureclockresponse-Methode

Die **setsecureclockresponse** -Methode legt die Antwort auf die sichere Uhr fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbresponse* \[ in\]
</dt> <dd>

Die festzulegende sichere Uhr-Antwort.

</dd> <dt>

*cbresponse* \[ in\]
</dt> <dd>

Die angegebene Größe der sicheren Uhr-Antwort in Bytes.

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

[**Getsecureclock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**Iwmdrmdevice-Schnittstelle**](iwmdrmdevice.md)
</dt> </dl>

 

 





