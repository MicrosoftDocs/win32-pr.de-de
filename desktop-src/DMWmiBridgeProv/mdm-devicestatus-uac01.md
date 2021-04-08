---
title: MDM_DeviceStatus_UAC01-Klasse
description: Die MDM \_ DeviceStatus \_ UAC01-Klasse wird vom Unternehmen verwendet, um den UAC-Status von Geräten mit ihren Unternehmensrichtlinien abzufragen.
ms.assetid: fb1ca1bb-229e-4eaa-a1e3-e790c1dab760
keywords:
- MDM_DeviceStatus_UAC01-Klasse
- MDM_DeviceStatus_UAC01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_UAC01
- MDM_DeviceStatus_UAC01.InstanceID
- MDM_DeviceStatus_UAC01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eecba42cd97bee660f66570e7f96c1ab2799f85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742617"
---
# <a name="mdm_devicestatus_uac01-class"></a>MDM \_ DeviceStatus \_ UAC01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die **MDM \_ DeviceStatus \_ UAC01** -Klasse wird vom Unternehmen verwendet, um den UAC-Status von Geräten mit ihren Unternehmensrichtlinien abzufragen.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_UAC01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a>Member

Die **MDM \_ DeviceStatus \_ UAC01** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ DeviceStatus \_ UAC01** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Knoten für die UAC-Abfrage.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Beschreibt den vollständigen Pfad zum übergeordneten Knoten. Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/DeviceStatus".

</dd> <dt>

[Status](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

