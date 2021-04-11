---
title: MDM_DeviceStatus_Compliance01-Klasse
description: Mit der MDM \_ DeviceStatus \_ Compliance01-Klasse können Sie Abfragen, ob das Gerät mit der Unternehmens Verschlüsselungs Richtlinie konform ist.
ms.assetid: 99c4cb9b-ae53-432c-b970-d61fb8496123
keywords:
- MDM_DeviceStatus_Compliance01-Klasse
- MDM_DeviceStatus_Compliance01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Compliance01
- MDM_DeviceStatus_Compliance01.InstanceID
- MDM_DeviceStatus_Compliance01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf606b7f10fbe7abc196622ee54b271e5285f2c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105008"
---
# <a name="mdm_devicestatus_compliance01-class"></a>MDM \_ DeviceStatus \_ Compliance01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Mit der **MDM \_ DeviceStatus \_ Compliance01** -Klasse können Sie Abfragen, ob das Gerät mit der Unternehmens Verschlüsselungs Richtlinie konform ist.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Compliance01
{
  string  InstanceID;
  string  ParentID;
  boolean EncryptionCompliance;
};
```

## <a name="members"></a>Member

Die **MDM \_ DeviceStatus \_ Compliance01** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ DeviceStatus \_ Compliance01** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Verschlüsselung](/windows/client-management/mdm/devicestatus-csp#devicestatus-compliance-encryptioncompliance)
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Knoten für Kompatibilitäts Abfragen.

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

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                      |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Dmwmibridgeprov. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von PowerShell-Skripts mit dem WMI-Bridge Anbieter](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

