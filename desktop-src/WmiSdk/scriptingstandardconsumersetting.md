---
description: Die Singleton ScriptingStandardConsumerSetting-Klasse stellt Registrierungsdaten bereit, die allen Instanzen der ActiveScriptEventConsumer-Standardconsumer-Consumerklasse gemeinsam sind.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: ScriptingStandardConsumerSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: a69d30511d01fba2df39483d1f76616bfae7c92812ce75989fd0c23558558b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316204"
---
# <a name="scriptingstandardconsumersetting-class"></a>ScriptingStandardConsumerSetting-Klasse

Die Singleton **ScriptingStandardConsumerSetting-Klasse** stellt Registrierungsdaten bereit, die allen Instanzen der [**ActiveScriptEventConsumer-Standardconsumer-Consumerklasse**](activescripteventconsumer.md) gemeinsam sind. Eine **ActiveScriptEventConsumer-Instanz** verwendet die **Eigenschaften MaximumScripts** und **Timeout.** Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md)

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

## <a name="syntax"></a>Syntax

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a>Member

Die **ScriptingStandardConsumerSetting-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ScriptingStandardConsumerSetting-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](standard-qualifiers.md) (64)
</dt> </dl>

Eine kurze Beschreibung eines Objekts, eine einzeilige Zeichenfolge. Enthält die Zeichenfolge **ScriptingStandardConsumerSetting,** da dies eine Singletonklasse ist.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Textbeschreibung eines Objekts.

</dd> <dt>

**MaximumScripts**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Maximale Anzahl von Skripts, die ausgeführt werden, bevor ein Consumer eine neue Instanz startet. Fahren Sie den Consumer regelmäßig herunter, um Speicherverluste durch Skripts zu löschen. Der Standardwert ist 300.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner für das Einstellungsobjekt.

</dd> <dt>

**Timeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Einheiten**](standard-qualifiers.md) ("Minuten")
</dt> </dl>

Maximale Anzahl von Minuten, bevor ein Consumer eine neue Instanz startet. Bei 0 (null) steuert die **MaximumScripts-Eigenschaft** die Lebensdauer des Consumers. Der gültige Bereich für **Timeout** ist 0 bis 71.000, und der Standardwert ist 0 (null).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die einzelne Instanz der **ScriptingStandardConsumerSetting-Klasse** befindet sich im \\ cimv2-Stammnamespace.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\Stammabonnement<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Einstellung**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[Standard-Consumerklassen](standard-consumer-classes.md)
</dt> <dt>

[Ausführen eines Skripts basierend auf einem Ereignis](running-a-script-based-on-an-event.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[Empfangen von Ereignissen zu jedem Zeitpunkt](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

