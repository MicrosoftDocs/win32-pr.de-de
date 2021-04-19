---
title: INapComponentConfig3 setconfigtoid-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um die Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Setconfigtoid-Methode NAP
- Setconfigtoid-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, setconfigtoid-Methode
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
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342674"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a>INapComponentConfig3:: setconfigtoid-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **setconfigtoid** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um die Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen.

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

*ConfigID* \[ in\]
</dt> <dd>

Ein-Wert, der die Konfiguration darstellt. *ConfigID* wird vom Netzwerk Richtlinien Server-Dienst (Network Policy Server, NPS) zugewiesen und ist innerhalb des SHV eindeutig. Wenn *ConfigID* den Wert 0 hat, wird die Standardkonfiguration des SHV festgelegt.

</dd> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Die Größe der Konfigurationsdaten in *Daten* in Bytes.

</dd> <dt>

*Daten* \[ in\]
</dt> <dd>

Bei Eingabe ein Bytearray, das das Konfigurations DataSet auf *ConfigID* enthält.

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

 

 





