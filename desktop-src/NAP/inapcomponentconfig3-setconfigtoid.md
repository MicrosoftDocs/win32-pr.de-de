---
title: INapComponentConfig3 SetConfigToID-Methode (NapCommon.h)
description: Wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Festlegen der Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- SetConfigToID-Methode NAP
- SetConfigToID-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3-Schnittstelle NAP, SetConfigToID-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010fdc6cbb236a113e4f1804d3a4780c0e6a72f89b1f03bf90f1d99a92dc2bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781080"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>INapComponentConfig3::SetConfigToID-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **SetConfigToID-Methode** wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Festlegen der Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*configID* \[ In\]
</dt> <dd>

Ein -Wert, der die Konfiguration darstellt. *ConfigID* wird vom NPS-Dienst (Network Policy Server) zugewiesen und ist innerhalb der SHV eindeutig. Wenn *ConfigID* 0 ist, wird die Standardkonfiguration der SHV festgelegt.

</dd> <dt>

*count* \[ In\]
</dt> <dd>

Die Größe der Konfigurationsdaten in den Daten in *Bytes.*

</dd> <dt>

*data* \[ In\]
</dt> <dd>

Bei der Eingabe ein BYTE-Array, das das Konfigurationsdatensatz auf *ConfigID enthält.*

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

 

 





