---
description: Die commandlineeventconsumer-Klasse führt ein angegebenes ausführbares Programm von einer Befehlszeile aus, wenn ein bestimmtes Ereignis auftritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Ausführen eines Programms von der Befehlszeile auf der Grundlage eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347069"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Ausführen eines Programms von der Befehlszeile auf der Grundlage eines Ereignisses

Die [**commandlineeventconsumer**](commandlineeventconsumer.md) -Klasse führt ein angegebenes ausführbares Programm von einer Befehlszeile aus, wenn ein bestimmtes Ereignis auftritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.

Wenn Sie [**commandlineeventconsumer**](commandlineeventconsumer.md)verwenden, sollten Sie die ausführbare Datei sichern, die Sie starten möchten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder nicht mit einer starken Zugriffs Steuerungs Liste (ACL) geschützt ist, kann ein Benutzer ohne Zugriffsberechtigungen die ausführbare Datei durch eine andere ausführbare Datei ersetzen. Sie können die [**Win32 \_ logicalfilesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) -oder [**Win32 \_ logicalsharesecuritysetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) -Klassen verwenden, um die Sicherheit einer Datei oder Freigabe Programm gesteuert zu ändern. Weitere Informationen finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

Die grundlegende Vorgehensweise für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern. Das folgende Verfahren fügt der grundlegenden Prozedur, ist spezifisch für die [**commandlineeventconsumer**](commandlineeventconsumer.md) -Klasse, und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Programm ausführt.

> [!Caution]
>
> Die [**commandlineeventconsumer**](commandlineeventconsumer.md) -Klasse verfügt über besondere Sicherheitseinschränkungen. Dieser Standardconsumer muss von einem lokalen Mitglied der Gruppe "Administratoren" auf dem lokalen Computer konfiguriert werden. Wenn Sie ein Domänen Konto zum Erstellen des Abonnements verwenden, muss das LocalSystem-Konto über die erforderlichen Berechtigungen für die Domäne verfügen, um sicherzustellen, dass der Ersteller Mitglied der lokalen Administratoren Gruppe ist.
>
> [**Commandlineeventconsumer**](commandlineeventconsumer.md) kann nicht verwendet werden, um einen Prozess zu starten, der interaktiv ausgeführt wird.

 

Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisconsumer erstellen, der einen Prozess über eine Befehlszeile ausführt.

**So erstellen Sie einen Ereignisconsumer, der einen Prozess über eine Befehlszeile ausführt**

1.  Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**commandlineeventconsumer**](commandlineeventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern. Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).
2.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und benennen Sie Sie mit einem Namen.
3.  Erstellen Sie eine Abfrage, um den Ereignistyp anzugeben. Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).
4.  Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der Instanz von [**commandlineeventconsumer**](commandlineeventconsumer.md)zuzuordnen.
5.  Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird eine neue Klasse mit dem Namen "mycmdlineconsumer" erstellt, um Ereignisse zu generieren, wenn eine Instanz der neuen Klasse am Ende einer MOF-Klasse erstellt wird. Das Beispiel ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen.

Im folgenden Verfahren wird beschrieben, wie eine neue Klasse mit dem Namen mycmdlineconsumer erstellt wird.

**So erstellen Sie eine neue Klasse mit dem Namen mycmdlineconsumer**

1.  Erstellen Sie die Datei c: \\ CmdLine \_test.bat mit einem Befehl, der ein sichtbares Programm ausführt, z. b. "calc.exe".
2.  Kopieren Sie die MOF-Datei in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.
3.  Kompilieren Sie in einem Befehlsfenster die MOF-Datei mit dem folgenden Befehl: " **Datei Name Dateiname. MOF**".

> [!Note]  
> Das in der cmdline- \_test.bat angegebene Programm sollte ausgeführt werden.

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
