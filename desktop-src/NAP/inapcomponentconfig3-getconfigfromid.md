---
title: INapComponentConfig3 getconfigfromid-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Getconfigfromid-Methode NAP
- Getconfigfromid-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, getconfigfromid-Methode
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
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740937"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a>INapComponentConfig3:: getconfigfromid-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getconfigfromid** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.

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

*ConfigID* \[ in\]
</dt> <dd>

Ein-Wert, der die Konfiguration darstellt. Wenn *ConfigID* den Wert **0** hat, sollte der SHV die Standard Konfigurationsdaten in *OutData* zurückgeben.

</dd> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Die Größe (in Bytes) der Konfigurationsdaten, die in *OutData* zurückgegeben werden.

</dd> <dt>

*OutData* \[ vorgenommen\]
</dt> <dd>

Bei der Rückgabe ein Bytearray, das die von der *ConfigID* dargestellten Konfigurationsdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                    | Beschreibung                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Der Vorgang ist erfolgreich.<br/> |
| <dl> <dt>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ nicht \_ gefunden**</dt> </dl> | *ConfigID* kann nicht gefunden werden.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Die [**newconfig**](inapcomponentconfig3-newconfig.md) -Methode muss verwendet werden, um Konfigurationsdaten für die *ConfigID* zuzuordnen, bevor diese Methode aufgerufen werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





