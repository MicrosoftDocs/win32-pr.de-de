---
title: MDM_WindowsAdvancedThreatProtection_DeviceTagging01-Klasse
description: Die MDM \_ windowsadvancedfixprotection \_ DeviceTagging01-Klasse wird verwendet, um die Integration, den Konfigurations-und Integritäts Status und die offboardendpunkte für Windows Defender Advanced Threat Protection zu integrieren.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01-Klasse
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01-Klasse, beschrieben
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 12cf3863ba67f422b42572a6934807d86abbc0e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104943"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a>MDM \_ windowsadvancedo Protection \_ DeviceTagging01-Klasse

\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können. Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]

Die MDM \_ windowsadvancedfixprotection \_ DeviceTagging01-Klasse wird verwendet, um die Integration, den Konfigurations-und Integritäts Status und die offboardendpunkte für Windows Defender Advanced Threat Protection zu integrieren.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a>Member

Die **MDM \_ windowsadvancedo Protection \_ DeviceTagging01** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MDM \_ windowsadvancedbedrohlich Protection \_ DeviceTagging01** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

[Wichtigkeit](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

[Gruppieren](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

</dd> <dt>

**Idmethod**
</dt> <dd> <dl> <dt>

Datentyp: **sint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

TBD

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                       |
| Namespace<br/>                | Root \\ CIMV2 \\ MDM- \\ dmmap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

