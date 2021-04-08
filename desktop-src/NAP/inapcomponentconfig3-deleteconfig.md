---
title: INapComponentConfig3 DeleteConfig-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- DeleteConfig-Methode NAP
- DeleteConfig-Methode, NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, DeleteConfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740945"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a>INapComponentConfig3::D eleteconfig-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **DeleteConfig** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten. Die ID kann wieder verwendet werden, nachdem die Konfigurationsdaten gelöscht wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigID* 
</dt> <dd>

Ein-Wert, der die zu löschenden Konfigurationsdaten darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Der Vorgang ist erfolgreich.<br/>                                      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                   | *ConfigID* ist 0 (ein Wert, der für die Standardkonfiguration reserviert ist).<br/> |
| <dl> <dt>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ nicht \_ gefunden**</dt> </dl> | *ConfigID* kann nicht gefunden werden.<br/>                                       |



 

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

 

 





