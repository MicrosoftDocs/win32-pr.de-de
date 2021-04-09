---
title: INapComponentConfig3 newconfig-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Newconfig-Methode, NAP
- Newconfig-Methode, NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, newconfig-Methode
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
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103298"
---
# <a name="inapcomponentconfig3newconfig-method"></a>INapComponentConfig3:: newconfig-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **newconfig** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten. Wenn diese Funktion aufgerufen wird, muss ein SHV neue Konfigurationsdaten zuordnen und diese mit einer Kopie der Standard Konfigurationsdaten auffüllen.

## <a name="syntax"></a>Syntax


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ConfigID* 
</dt> <dd>

Ein-Wert, der die Konfiguration darstellt. *ConfigID* wird vom Netzwerk Richtlinien Server-Dienst (Network Policy Server, NPS) zugewiesen und ist innerhalb des SHV eindeutig.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                 | Beschreibung                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Der Vorgang ist erfolgreich.<br/>                                                       |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                | *ConfigID* ist 0 (ein Wert, der für die Standardkonfiguration reserviert ist).<br/>                  |
| <dl> <dt>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ vorhanden**</dt> </dl> | Die *ConfigID* ist bereits vorhanden. Die Liste der IDs, die NPS bekannt sind, unterscheidet sich vom SHV.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Nachdem die neue Konfiguration von **newconfig** erstellt wurde, sollten die Methoden [**getconfigfromid**](inapcomponentconfig3-getconfigfromid.md), [**invokeuifromconfigblob**](inapcomponentconfig2-invokeuifromconfigblob.md)und [**setconfigtoid**](inapcomponentconfig3-setconfigtoid.md) verwendet werden, um die Konfiguration nach Bedarf zu ändern.

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

 

 





