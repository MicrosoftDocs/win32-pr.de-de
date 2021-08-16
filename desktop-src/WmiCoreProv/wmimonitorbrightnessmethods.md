---
description: Enthält Methoden, die die Überwachung der Helligkeit verwalten.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: WmiMonitorBrightnessMethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 255cfa75ab892739ce211432ef81d32da4e1cbb3205e5467045e2d81f156d102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321362"
---
# <a name="wmimonitorbrightnessmethods-class"></a>WmiMonitorBrightnessMethods-Klasse

Die WMI-Klasse **WmiMonitorBrightnessMethods** enthält Methoden, die die Helligkeit des Monitors verwalten.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Member

Die **WmiMonitorBrightnessMethods-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#wmimonitorbrightnessmethods-class)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **WmiMonitorBrightnessMethods-Klasse** verfügt über diese Methoden.



| Methode                                                                                                         | Beschreibung                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | Legt die Helligkeit wieder auf die Richtlinieneinstellung fest.<br/>     |
| [**WmiSetALSBrightness**](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | Legt den Helligkeitswert des Umgebungslichtsensors fest.<br/>     |
| [**WmiSetALSBrightnessState**](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | Steuert den Helligkeitszustand des Umgebungslichtsensors.<br/> |
| [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | Legt die Helligkeit des Monitors fest.<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorBrightnessMethods-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der spezifischen Überwachungsinstanz.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




