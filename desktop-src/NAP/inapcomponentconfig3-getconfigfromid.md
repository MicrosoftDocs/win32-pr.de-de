---
title: INapComponentConfig3 GetConfigFromID-Methode (NapCommon.h)
description: Wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- GetConfigFromID-Methode NAP
- GetConfigFromID-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3-Schnittstelle NAP, GetConfigFromID-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 638704b5706b68b67f854a6a52b6c845be3fb757b596e9f5425f315c7d679fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368381"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>INapComponentConfig3::GetConfigFromID-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **GetConfigFromID-Methode** wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*configID* \[ In\]
</dt> <dd>

Ein -Wert, der die Konfiguration darstellt. Wenn *ConfigID* **0 ist,** sollte die SHV die Standardkonfigurationsdaten in *outdata zurückgeben.*

</dd> <dt>

*count* \[ out\]
</dt> <dd>

Die Größe der in outdata zurückgegebenen Konfigurationsdaten in *Bytes.*

</dd> <dt>

*outdata* \[ out\]
</dt> <dd>

Bei der Rückgabe ein BYTE-Array, das die durch ConfigID dargestellten *Konfigurationsdaten enthält.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                                    | Beschreibung                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Der Vorgang ist erfolgreich.<br/> |
| <dl> <dt>**NAP \_ E \_ \_ SHV-KONFIGURATION NICHT \_ \_ GEFUNDEN**</dt> </dl> | *ConfigID* wurde nicht gefunden.<br/>  |



 

## <a name="remarks"></a>Hinweise

Die [**NewConfig-Methode**](inapcomponentconfig3-newconfig.md) muss zum Zuordnen von Konfigurationsdaten für *ConfigID verwendet* werden, bevor diese Methode aufgerufen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





