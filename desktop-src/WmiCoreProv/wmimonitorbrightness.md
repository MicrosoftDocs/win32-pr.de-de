---
description: Stellt die Helligkeitsparameter eines Computermonitors dar.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: WmiMonitorBrightness-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 10343b33e5bc1881440af9d13029913d470880289e71b4c7a33fb4748e56ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821521"
---
# <a name="wmimonitorbrightness-class"></a>WmiMonitorBrightness-Klasse

Die **WMI-Klasse WmiMonitorBrightness** stellt die Helligkeitsparameter eines Computermonitors dar.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a>Member

Die **WmiMonitorBrightness-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorBrightness-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Zielmonitor aktiv ist.

</dd> <dt>

**CurrentBrightness**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktuelle Helligkeit. Bei diesem Wert muss es sich um einen Wert aus *Ebenen* handelt.

Beispiel: 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: Schlüssel
</dt> </dl>

Name der spezifischen Überwachungsinstanz.

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array, das die möglichen Helligkeitsstufen enthält.

Beispiel: \[ 0, 1, 2, ..., 100 \] .

</dd> <dt>

**Ebenen**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl von Helligkeitsstufen, die der Monitor unterstützt, wie unter *Ebene* beschrieben.

Beispiel: 101

</dd> </dl>

## <a name="examples"></a>Beispiele

Weitere Informationen und Codebeispiele zur Verwendung dieser Klasse in PowerShell finden Sie unter [Verwenden von PowerShell zum Melden und Festlegen](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)der Helligkeit des Monitors.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




