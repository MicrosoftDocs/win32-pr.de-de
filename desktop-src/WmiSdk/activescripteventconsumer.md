---
description: Führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis zugestellt wird.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Activescripteventconsumer-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362880"
---
# <a name="activescripteventconsumer-class"></a>Activescripteventconsumer-Klasse

Die **activescripteventconsumer** -Klasse führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis an Sie übermittelt wird. Diese Klasse ist einer der standardereignisconsumer, die von WMI bereitstellt werden. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



Sie können die Leistung aller Instanzen von **activescripteventconsumer** in einem System konfigurieren, indem Sie die Werte der Eigenschaft [**Timeout**](scriptingstandardconsumersetting.md) oder **maximumscripts** in der einzelnen Instanz von **scriptingstandardconsumersetting** festlegen.

## <a name="syntax"></a>Syntax

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a>Member

Die **activescripteventconsumer** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **activescripteventconsumer** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**"Kreatorsid"**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array, das die Sicherheits-ID (SID) darstellt, die den Ersteller des aktiven Skript-Ereignisconsumers eindeutig identifiziert. Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Killtimeout**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl in Sekunden, für die das Skript ausgeführt werden darf. Wenn der Standardwert 0 (null) ist, wird das Skript nicht beendet.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name des Computers, an den WMI Ereignisse sendet. Gemäß der Konvention von Microsoft-Standard Verbrauchern kann der Skript Consumer nicht remote ausgeführt werden. Consumer von Drittanbietern können diese Eigenschaft ebenfalls verwenden. Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange in Bytes für den aktiven Skript-Ereignisconsumer. Diese Eigenschaft wird von [**\_ \_ eventconsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Eindeutiger Bezeichner für den Ereignisconsumer. Wenn Sie den Consumer umbenennen, ist das Ergebnis zwei gleichwertige Consumer mit unterschiedlichen Namen.

</dd> <dt>

**Scriptfilename**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Datei, aus der der Skript Text gelesen wird. Sie dient als Alternative zum Angeben des Skript Texts in der **ScriptText** -Eigenschaft. Diese Eigenschaft muss **null** sein, wenn die **ScriptText** -Eigenschaft nicht **null** ist.

> [!Note]  
> Wenn Sie **scriptfilename** angeben, ist es wichtig, die ausführbare Datei zu sichern, die Sie starten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder durch eine sichere Zugriffs Steuerungs Liste (ACL) geschützt ist, kann jeder Benutzer die ausführbare Datei durch eine andere ersetzen. Weitere Informationen zu ACLs finden Sie unter [Erstellen eines Sicherheits Deskriptors (SD) für ein neues Objekt in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**Scriptingengine**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der zu verwendenden Skript-Engine, z. b. "VBScript". Diese Eigenschaft darf nicht **null** sein.

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Text des Skripts, das in einer Sprache ausgedrückt wird, die der Skript-Engine bekannt ist. Diese Eigenschaft muss **null** sein, wenn die **scriptfilename** -Eigenschaft nicht **null** ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von der [**\_ \_ eventconsumer**](--eventconsumer.md) abstract-Klasse abgeleitet. Sie befindet sich im \\ Namespace des Stamm Abonnements.

Wenn der Text eines Skripts in der ereignisconsumerinstanz angegeben ist, hat das Skript Zugriff auf die Ereignis Instanz in der Skript Umgebungsvariablen **targetevent**.

Die Skripts werden im Sicherheitskontext "LocalSystem" ausgeführt. Als Sicherheitsmaßnahme kann der skriptingconsumer nur von einem lokalen Systemadministrator oder einem Domänen Administrator konfiguriert werden. Zugriffsrechte werden bis zur Laufzeit nicht geprüft. Nachdem der Consumer konfiguriert wurde, kann jeder Benutzer das Ereignis, das das Skript verursacht, auslöst.

Fehler beim Laden der Skript-Engine oder beim Analysieren und Validieren des Skripts werden als Fehler betrachtet. Fehlerrückgabe Codes aus dem Skript und das Beenden des Skripts mit einem Timeout werden ebenfalls als Fehler betrachtet.

Entweder ' **ScriptText** ' oder ' **scriptfilename** ' darf nicht **null** sein. Wenn beide Eigenschaften **null** oder nicht **null** sind, wird ein Fehler generiert.

Wenn WMI als Dienst ausgeführt wird, generieren Skripts, die von **activescripteventconsumer** ausgeführt werden, keine Bildschirmausgabe. Skripts, die **MsgBox** verwenden, werden nicht auf dem Bildschirm angezeigt. Das Ausführen des WMI-Dienstanbieter als ausführbare Datei wird nicht unterstützt, aber WMI ermöglicht es Skripts, die die **MsgBox** -Funktion verwenden, Ausgaben anzuzeigen oder Benutzereingaben zu akzeptieren. Keine der vom [WScript](/previous-versions//at5ydy31(v=vs.85)) -Objekt bereitgestellten Methoden kann verwendet werden, da **activescripteventconsumer** Windows Script Host (WSH) nicht verwendet.

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel [Erstellen permanenter WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **activescripteventconsumer** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Stamm \\ Abonnement<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Standard Consumer-Klassen](standard-consumer-classes.md)
</dt> <dt>

[Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md)
</dt> <dt>

[Empfangen von Ereignissen zu allen Zeitpunkten](receiving-events-at-all-times.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[**\_\_Eventconsumer**](--eventconsumer.md)
</dt> <dt>

[**Scriptingstandardconsumersetting**](scriptingstandardconsumersetting.md)
</dt> </dl>

 

