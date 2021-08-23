---
title: INapComponentConfig3 NewConfig-Methode (NapCommon.h)
description: Wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID bereitzustellen.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- NewConfig-Methode NAP
- NewConfig-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3-Schnittstelle NAP, NewConfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff87f55218d8c84b1cb95a75e1801783e57b17288c36057323589ab44a47d3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891340"
---
# <a name="inapcomponentconfig3newconfig-method"></a>INapComponentConfig3::NewConfig-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **NewConfig-Methode** wird von System health validators (SHVs) implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID bereitzustellen. Wenn diese Funktion aufgerufen wird, muss eine SHV neue Konfigurationsdaten zuordnen und mit einer Kopie der Standardkonfigurationsdaten auffüllen.

## <a name="syntax"></a>Syntax


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*configID* 
</dt> <dd>

Ein -Wert, der die Konfiguration darstellt. *ConfigID* wird vom NpS-Dienst (Network Policy Server) zugewiesen und ist innerhalb der SHV eindeutig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                 | Beschreibung                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Der Vorgang ist erfolgreich.<br/>                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                | *ConfigID* ist 0 (ein für die Standardkonfiguration reservierter Wert).<br/>                  |
| <dl> <dt>**NAP \_ E \_ SHV \_ CONFIG \_ EXISTED**</dt> </dl> | *ConfigID* ist bereits vorhanden. Die Liste der IDs, die NPS bekannt sind, unterscheidet sich von der SHV.<br/> |



 

## <a name="remarks"></a>Hinweise

Nachdem die neue Konfiguration von **NewConfig** erstellt wurde, sollten die Methoden [**GetConfigFromID,**](inapcomponentconfig3-getconfigfromid.md) [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)und [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) verwendet werden, um die Konfiguration nach Bedarf zu ändern.

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

 

 





