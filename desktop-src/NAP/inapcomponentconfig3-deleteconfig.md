---
title: INapComponentConfig3 DeleteConfig-Methode (NapCommon.h)
description: Wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- DeleteConfig-Methode NAP
- DeleteConfig-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3-Schnittstelle NAP, DeleteConfig-Methode
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
ms.openlocfilehash: 07b7d0772f8ee8ff0735c7d95dad259c9c7697fde426ce52768d554011bd1680
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799725"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a>INapComponentConfig3::D eleteConfig-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **DeleteConfig-Methode** wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten. Die ID kann wiederverwendet werden, nachdem die Konfigurationsdaten gelöscht wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*configID* 
</dt> <dd>

Ein -Wert, der die zu löschenden Konfigurationsdaten darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Fehlercodes basierend auf dem Ergebnis dieses Vorgangs zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                          | Der Vorgang ist erfolgreich.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                   | *ConfigID ist* 0 (ein Wert, der für die Standardkonfiguration reserviert ist).<br/> |
| <dl> <dt>**NAP \_ E \_ \_ SHV-KONFIGURATION NICHT \_ \_ GEFUNDEN**</dt> </dl> | *ConfigID* wurde nicht gefunden.<br/>                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapComponentConfig3**](inapcomponentconfig3.md)
</dt> </dl>

 

 





