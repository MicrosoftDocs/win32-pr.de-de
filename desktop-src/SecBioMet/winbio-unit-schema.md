---
title: WINBIO_UNIT_SCHEMA Struktur (winbio \_ types. h)
description: Beschreibt die Funktionen einer biometrischen Einheit.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- WINBIO_UNIT_SCHEMA Struktur Windows-Biometrieframework-API
- PWINBIO_UNIT_SCHEMA Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_UNIT_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c217be1e0c6bde740c815f5a990509a6a87ef0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957155"
---
# <a name="winbio_unit_schema-structure"></a>Struktur des winbio- \_ Einheiten \_ Schemas

Die Struktur der **winbio- \_ Einheiten \_ Schema** beschreibt die Funktionen einer biometrischen Einheit. Sie wird von der [**winbioenumbiometricunits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) -Funktion verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_UNIT_SCHEMA {
  WINBIO_UNIT_ID                  UnitId;
  WINBIO_POOL_TYPE                PoolType;
  WINBIO_BIOMETRIC_TYPE           BiometricFactor;
  WINBIO_BIOMETRIC_SENSOR_SUBTYPE SensorSubType;
  WINBIO_CAPABILITIES             Capabilities;
  WINBIO_STRING                   DeviceInstanceId;
  WINBIO_STRING                   Description;
  WINBIO_STRING                   Manufacturer;
  WINBIO_STRING                   Model;
  WINBIO_STRING                   SerialNumber;
  WINBIO_VERSION                  FirmwareVersion;
} WINBIO_UNIT_SCHEMA, *PWINBIO_UNIT_SCHEMA;
```



## <a name="members"></a>Member

<dl> <dt>

**Unitid**
</dt> <dd>

Ein-Wert, der die biometrische Einheit identifiziert.

</dd> <dt>

**Pooltyp**
</dt> <dd>

Ein **ulong** -Wert, der den Typ der biometrischen Einheit angibt. Mögliche Werte:



| Wert                                                                                                                                                                            | Bedeutung                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**winbio- \_ Pool \_ unbekannt**</dt> </dl> | Der Typ ist unbekannt.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**winbio- \_ Pool \_ System**</dt> </dl>    | Die Sitzung stellt eine Verbindung mit einer freigegebenen Sammlung von biometrischen Einheiten her, die vom Dienstanbieter verwaltet werden.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**privater winbio- \_ Pool \_**</dt> </dl> | Die Sitzung stellt eine Verbindung mit einer Sammlung von biometrischen Einheiten her, die vom Aufrufer verwaltet werden.<br/>         |



 

</dd> <dt>

**Biometricfactor**
</dt> <dd>

Ein-Wert, der den Typ der biometrischen Einheit angibt. Derzeit wird nur der **winbio- \_ \_ typfingerabdruck** unterstützt.

</dd> <dt>

**Sensorsubtype**
</dt> <dd>

Ein Sensor Untertyp, der für den biometrischen Typ definiert ist, der vom **biometricfactor** -Member angegeben wird. Derzeit werden nur Fingerabdruck Typen (**winbio- \_ \_ typfingerabdruck**) unterstützt. Die folgenden Untertypen sind zurzeit für Fingerabdrücke definiert:

-   der winbio- \_ Sensor \_ Untertyp ist \_ unbekannt.
-   winbio- \_ FP- \_ \_ unter Typ \_ schwenken
-   Fingereingabe von winbio \_ FP- \_ Sensor \_ unter Typ \_

</dd> <dt>

**Capabilities**
</dt> <dd>

Eine Bitmaske der Funktionen des biometrischen Sensors. Hierbei kann es sich um einen bitweisen **oder** um die folgenden Werte handeln:

-   winbio- \_ Fähigkeits \_ Sensor
-   winbio-Funktions Vergleich \_ \_
-   winbio-Funktions \_ \_ Datenbank
-   Verarbeitung von winbio- \_ Funktionen \_
-   Verschlüsselung von winbio- \_ Funktionen \_
-   Navigation in winbio- \_ Funktionen \_
-   winbio-Funktions \_ \_ Indikator
-   virtueller winbio- \_ Fähigkeits \_ \_ Sensor
    > [!Note]  
    > Die **\_ \_ virtuelle \_ Sensor Konstante für winbio-Funktionen** gilt nur für Windows 10 und höher.

     

</dd> <dt>

**Geräte-ID**
</dt> <dd>

Ein Zeichen folgen Wert, der die Geräte-ID enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.

</dd> <dt>

**Beschreibung**
</dt> <dd>

Ein Zeichen folgen Wert, der eine Beschreibung der biometrischen Einheit enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.

</dd> <dt>

**Manufacturer**
</dt> <dd>

Ein Zeichen folgen Wert, der den Namen des Herstellers enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.

</dd> <dt>

**Modell**
</dt> <dd>

Ein Zeichen folgen Wert, der die Modellnummer der biometrischen Einheit enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.

</dd> <dt>

**SerialNumber**
</dt> <dd>

Eine **null**-terminierte Unicode-Zeichenfolge, die die Seriennummer der biometrischen Einheit enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen einschließlich eines abschließenden **null** -Zeichens enthalten.

</dd> <dt>

**Firmwareversion**
</dt> <dd>

Eine [**winbio- \_ Versions**](winbio-version.md) Struktur, die die Haupt-und neben Versionsnummern für die biometrische Einheit enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> <dt>

[**Winbioenumbiometricunits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





