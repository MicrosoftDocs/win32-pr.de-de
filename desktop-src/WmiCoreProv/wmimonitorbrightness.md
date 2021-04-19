---
description: Stellt die Parameter für die Helligkeit eines Computermonitors dar.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Wmimonitorbrightness-Klasse
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
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369803"
---
# <a name="wmimonitorbrightness-class"></a>Wmimonitorbrightness-Klasse

Die **wmimonitorbrightness** WMI-Klasse stellt die Parameter für die Helligkeit eines Computermonitors dar.

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

Die **wmimonitorbrightness** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitorbrightness** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Ziel Monitor aktiv ist.

</dd> <dt>

**Currenthelligkeit**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Aktuelle Helligkeit. Dieser Wert muss ein Wert sein, der von *Ebenen* übernommen wird.

Beispiel: 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: Schlüssel
</dt> </dl>

Der Name der spezifischen Monitor Instanz.

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die möglichen Helligkeits Ebenen enthält.

Beispiel: \[ 0, 1, 2,..., 100 \] .

</dd> <dt>

**Ebenen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der vom Monitor unterstützten Helligkeitsstufen, wie unter *Ebene* beschrieben.

Beispiel: 101

</dd> </dl>

## <a name="examples"></a>Beispiele

Weitere Informationen und Codebeispiele zur Verwendung dieser Klasse in PowerShell finden Sie unter [Verwenden von PowerShell zum melden und Festlegen der Monitor Helligkeit](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




