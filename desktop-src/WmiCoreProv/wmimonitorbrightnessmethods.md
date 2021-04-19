---
description: Enthält Methoden, mit denen die Monitor Helligkeit verwaltet wird.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Wmimonitorbrightnessmethods-Klasse
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
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363578"
---
# <a name="wmimonitorbrightnessmethods-class"></a>Wmimonitorbrightnessmethods-Klasse

Die **wmimonitorbrightnessmethods** -WMI-Klasse enthält Methoden, mit denen die Monitor Helligkeit verwaltet wird.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Member

Die **wmimonitorbrightnessmethods** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#wmimonitorbrightnessmethods-class)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **wmimonitorbrightnessmethods** -Klasse verfügt über diese Methoden.



| Methode                                                                                                         | BESCHREIBUNG                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**Wmireverttopolicyhelligkeit**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | Legt die Helligkeit auf die Richtlinien Einstellung zurück.<br/>     |
| [**WMI-talshelligkeit**](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | Legt den Wert für Umgebungslichtsensor-Helligkeit fest.<br/>     |
| [**Wmiantalsbrightnessstate**](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | Steuert den Helligkeit-Zustand des Umgebungslicht Sensors.<br/> |
| [**Wmisethelligkeit**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | Legt die Helligkeit des Monitors fest.<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die **wmimonitorbrightnessmethods** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name der spezifischen Monitor Instanz.

</dd> </dl>

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

 

 




