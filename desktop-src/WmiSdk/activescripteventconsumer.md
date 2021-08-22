---
description: Führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis an das Skript übermittelt wird.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: ActiveScriptEventConsumer-Klasse
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
ms.openlocfilehash: acf7ef4b4207f72cbaee61c0aaad8b2279419682bdddbeb4373c36c6868b8fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557833"
---
# <a name="activescripteventconsumer-class"></a>ActiveScriptEventConsumer-Klasse

Die **ActiveScriptEventConsumer-Klasse** führt ein vordefiniertes Skript in einer beliebigen Skriptsprache aus, wenn ein Ereignis an sie übermittelt wird. Diese Klasse ist einer der Standardereignis-Consumer, die WMI bereitstellt. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md)


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



Sie können die Leistung aller Instanzen von **ActiveScriptEventConsumer** auf einem System konfigurieren, indem Sie die Werte der [**Timeout-**](scriptingstandardconsumersetting.md) oder **MaximumScripts-Eigenschaft** in der einzelnen Instanz von **ScriptingStandardConsumerSetting** festlegen.

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

Die **ActiveScriptEventConsumer-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ActiveScriptEventConsumer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array, das die Sicherheits-ID (SID) darstellt, die den Ersteller des Active Script-Ereignis-Consumers eindeutig identifiziert. Diese Eigenschaft wird von [**\_ \_ EventConsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl in Sekunden, die das Skript ausführen darf. Wenn 0 (null) der Standardwert ist, wird das Skript nicht beendet.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name des Computers, an den WMI Ereignisse sendet. Nach der Konvention von Microsoft-Standardverbrauchern kann der Skript-Consumer nicht remote ausgeführt werden. Drittanbieter-Consumer können diese Eigenschaft auch verwenden. Diese Eigenschaft wird von [**\_ \_ EventConsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Maximale Warteschlange in Bytes für den Active Script-Ereignis-Consumer. Diese Eigenschaft wird von [**\_ \_ EventConsumer**](--eventconsumer.md)geerbt.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](standard-qualifiers.md)
</dt> </dl>

Eindeutiger Bezeichner für den Ereignisverbraucher. Wenn Sie den Consumer umbenennen, ergeben sich zwei identische Consumer mit unterschiedlichen Namen.

</dd> <dt>

**ScriptFileName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Datei, aus der der Skripttext gelesen wird. Er ist als Alternative zum Angeben des Skripttexts in der **ScriptText-Eigenschaft** vorgesehen. Diese Eigenschaft muss **NULL** sein, wenn die **ScriptText-Eigenschaft** nicht **NULL** ist.

> [!Note]  
> Wenn Sie **ScriptFileName** angeben, ist es wichtig, die ausführbare Datei zu schützen, die Sie starten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder mit einer Starken Zugriffssteuerungsliste (Strong Access Control List, ACL) geschützt ist, kann jeder die ausführbare Datei durch eine andere ersetzen. Weitere Informationen zu ACLs finden Sie unter [Erstellen eines Sicherheitsdeskriptors (SD) für ein neues Objekt in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**ScriptingEngine**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name der zu verwendenden Skript-Engine, z. B. "VBScript". Diese Eigenschaft darf nicht **NULL** sein.

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Text des Skripts, der in einer Sprache ausgedrückt wird, die der Skript-Engine bekannt ist. Diese Eigenschaft muss **NULL** sein, wenn die **ScriptFileName-Eigenschaft** nicht **NULL** ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Klasse wird von der [**\_ \_ abstrakten EventConsumer-Klasse**](--eventconsumer.md) abgeleitet. Sie befindet sich im \\ Stammabonnementnamespace.

Wenn der Text eines Skripts in der Ereignisverbraucherinstanz angegeben wird, hat das Skript Zugriff auf die Ereignisinstanz in der Skriptumgebungsvariablen **TargetEvent**.

Die Skripts werden im Sicherheitskontext LocalSystem ausgeführt. Als Sicherheitsmaßnahme kann der Skriptbenutzer nur von einem lokalen Systemadministrator oder Domänenadministrator konfiguriert werden. Zugriffsrechte werden erst zur Laufzeit überprüft. Nachdem der Consumer konfiguriert wurde, kann jeder Benutzer das Ereignis auslösen, das das Skript zu veranlasst.

Ein Fehler beim Laden der Skript-Engine oder beim Analysieren und Überprüfen des Skripts wird als Fehler betrachtet. Fehlerrückgabecodes aus dem Skript und das Beenden des Skripts mithilfe eines Time outs werden ebenfalls als Fehler betrachtet.

**Entweder ScriptText** oder **ScriptFileName** darf nicht **NULL** sein. Wenn beide Eigenschaften **NULL** oder nicht **NULL** sind, wird ein Fehler generiert.

Wenn WMI als Dienst ausgeführt wird, generieren skripts, die von **ActiveScriptEventConsumer** ausgeführt werden, keine Bildschirmausgabe. Skripts, die **MsgBox** verwenden, werden zwar ausgeführt, zeigen aber keine Informationen auf dem Bildschirm an. Das Ausführen des WMI-Diensts als ausführbare Datei wird nicht unterstützt, aber WMI ermöglicht Skripts, die die **MsgBox-Funktion** verwenden, die Ausgabe anzuzeigen oder Benutzereingaben zu akzeptieren. Keine der vom [WScript-Objekt](/previous-versions//at5ydy31(v=vs.85)) bereitgestellten Methoden kann verwendet werden, da **ActiveScriptEventConsumer** nicht Windows Script Host (WSH) verwendet.

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in TechNet Gallery verwendet **ActiveScriptEventConsumer** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignisregistrierung einzurichten.

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

[Standard-Consumerklassen](standard-consumer-classes.md)
</dt> <dt>

[Ausführen eines Skripts basierend auf einem Ereignis](running-a-script-based-on-an-event.md)
</dt> <dt>

[Empfangen von Ereignissen zu jedem Zeitpunkt](receiving-events-at-all-times.md)
</dt> <dt>

[Erstellen eines logischen Consumers](creating-a-logical-consumer.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)
</dt> </dl>

 

