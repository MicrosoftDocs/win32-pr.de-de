---
title: WINBIO_UNIT_SCHEMA Struktur (Winbio \_ types.h)
description: Beschreibt die Funktionen einer biometrischen Einheit.
ms.assetid: b20adf18-2948-481f-9d12-8da17aa152f7
keywords:
- WINBIO_UNIT_SCHEMA Struktur Windows Biometrieframework-API
- PWINBIO_UNIT_SCHEMA Strukturzeiger Windows Biometrieframework-API
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
ms.openlocfilehash: ae91ae5353aa0e9c02414e90a8364d86bdc56c0cdcc4f4586656f28f92f100ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909169"
---
# <a name="winbio_unit_schema-structure"></a>WINBIO \_ UNIT \_ SCHEMA-Struktur

Die **WINBIO \_ UNIT \_ SCHEMA-Struktur** beschreibt die Funktionen einer biometrischen Einheit. Sie wird von der [**WinBioEnumBiometricUnits-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits) verwendet.

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

**UnitId**
</dt> <dd>

Ein -Wert, der die biometrische Einheit identifiziert.

</dd> <dt>

**PoolType**
</dt> <dd>

Ein **ULONG-Wert,** der den Typ der biometrischen Einheit angibt. Mögliche Werte:



| Wert                                                                                                                                                                            | Bedeutung                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_POOL_UNKNOWN"></span><span id="winbio_pool_unknown"></span><dl> <dt>**\_WINBIO-POOL \_ UNBEKANNT**</dt> </dl> | Der Typ ist unbekannt.<br/>                                                                            |
| <span id="WINBIO_POOL_SYSTEM"></span><span id="winbio_pool_system"></span><dl> <dt>**\_WINBIO-POOLSYSTEM \_**</dt> </dl>    | Die Sitzung stellt eine Verbindung mit einer freigegebenen Sammlung biometrischer Einheiten her, die vom Dienstanbieter verwaltet werden.<br/> |
| <span id="WINBIO_POOL_PRIVATE"></span><span id="winbio_pool_private"></span><dl> <dt>**WINBIO \_ POOL \_ PRIVATE**</dt> </dl> | Die Sitzung stellt eine Verbindung mit einer Sammlung biometrischer Einheiten her, die vom Aufrufer verwaltet werden.<br/>         |



 

</dd> <dt>

**BiometricFactor**
</dt> <dd>

Ein -Wert, der den Typ der biometrischen Einheit angibt. Derzeit wird nur **WINBIO \_ TYPE \_ FINGERPRINT** unterstützt.

</dd> <dt>

**SensorSubType**
</dt> <dd>

Ein Sensoruntertyp, der für den vom **BiometricFactor-Member** angegebenen biometrischen Typ definiert ist. Derzeit werden nur Fingerabdrucktypen **(WINBIO \_ TYPE \_ FINGERPRINT)** unterstützt. Die folgenden Untertypen sind derzeit für Fingerabdrücke definiert:

-   WINBIO \_ SENSOR \_ SUBTYPE \_ UNKNOWN
-   WINBIO \_ FP \_ SENSOR \_ SUBTYPE \_ SWIPE
-   WINBIO \_ FP \_ SENSOR \_ SUBTYPE \_ TOUCH

</dd> <dt>

**Capabilities**
</dt> <dd>

Eine Bitmaske der biometrischen Sensorfunktionen. Dies kann ein bitweises **OR** der folgenden Werte sein:

-   \_WINBIO-FUNKTIONSSENSOR \_
-   \_ \_ WINBIO-FUNKTIONSABGLEICH
-   \_WINBIO-FUNKTIONSDATENBANK \_
-   \_WINBIO-FUNKTIONSVERARBEITUNG \_
-   \_WINBIO-FUNKTIONSVERSCHLÜSSELUNG \_
-   \_WINBIO-FUNKTIONSNAVIGATION \_
-   \_WINBIO-FUNKTIONSINDIKATOR \_
-   \_ \_ VIRTUELLER WINBIO-FUNKTIONSSENSOR \_
    > [!Note]  
    > Die **KONSTANTE WINBIO \_ CAPABILITY VIRTUAL \_ \_ SENSOR** gilt nur für Windows 10 und höher.

     

</dd> <dt>

**DeviceInstanceId**
</dt> <dd>

Ein Zeichenfolgenwert, der die Geräte-ID enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen enthalten, einschließlich eines abschließenden **NULL-Zeichens.**

</dd> <dt>

**Beschreibung**
</dt> <dd>

Ein Zeichenfolgenwert, der eine Beschreibung der biometrischen Einheit enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen enthalten, einschließlich eines abschließenden **NULL-Zeichens.**

</dd> <dt>

**Manufacturer**
</dt> <dd>

Ein Zeichenfolgenwert, der den Namen des Herstellers enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen enthalten, einschließlich eines abschließenden **NULL-Zeichens.**

</dd> <dt>

**Modell**
</dt> <dd>

Ein Zeichenfolgenwert, der die Modellnummer der biometrischen Einheit enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen enthalten, einschließlich eines abschließenden **NULL-Zeichens.**

</dd> <dt>

**Serialnumber**
</dt> <dd>

Eine **Mit NULL** endende Unicode-Zeichenfolge, die die Seriennummer der biometrischen Einheit enthält. Die Zeichenfolge kann bis zu 256 Unicode-Zeichen enthalten, einschließlich eines abschließenden **NULL-Zeichens.**

</dd> <dt>

**FirmwareVersion**
</dt> <dd>

Eine [**\_ WINBIO-VERSIONSstruktur,**](winbio-version.md) die die Haupt- und Nebenversionsnummern für die biometrische Einheit enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WinBioEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioenumbiometricunits)
</dt> </dl>

 

 





