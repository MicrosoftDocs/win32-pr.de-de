---
description: Die CommandLineEventConsumer-Klasse führt ein angegebenes ausführbares Programm über eine Befehlszeile aus, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein Standardereignis-Consumer, den WMI bietet.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Ausführen eines Programms über die Befehlszeile basierend auf einem Ereignis
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c499713b3c6496759d94229e291138b0cb07de9e9f35d116eb19b4a7aeb3829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553968"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Ausführen eines Programms über die Befehlszeile basierend auf einem Ereignis

Die [**CommandLineEventConsumer-Klasse**](commandlineeventconsumer.md) führt ein angegebenes ausführbares Programm über eine Befehlszeile aus, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein Standardereignis-Consumer, den WMI bietet.

Wenn Sie [**CommandLineEventConsumer verwenden,**](commandlineeventconsumer.md)sollten Sie die ausführbare Datei sichern, die Sie starten möchten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder nicht mit einer starken Zugriffssteuerungsliste (ACL) geschützt ist, kann ein Benutzer ohne Zugriffsberechtigungen Ihre ausführbare Datei durch eine andere ausführbare Datei ersetzen. Sie können die [**Win32 \_ LogicalFileSecuritySetting-**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) oder [**Win32 \_ LogicalShareSecuritySetting-Klassen**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) verwenden, um die Sicherheit einer Datei oder Freigabe programmgesteuert zu ändern. Weitere Informationen finden Sie unter Creating a Security Descriptor for a New Object in C++ (Erstellen eines [Sicherheitsdeskriptors für ein neues Objekt in C++).](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

Das grundlegende Verfahren zur Verwendung von Standardverbrauchern ist immer identisch und befindet sich unter Überwachung und Reaktion auf Ereignisse [mit Standardverbrauchern.](monitoring-and-responding-to-events-with-standard-consumers.md) Die folgende Prozedur fügt der grundlegenden Prozedur hinzu, ist spezifisch für die [**CommandLineEventConsumer-Klasse**](commandlineeventconsumer.md) und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Programm ausgeführt.

> [!Caution]
>
> Die [**CommandLineEventConsumer-Klasse**](commandlineeventconsumer.md) verfügt über besondere Sicherheitseinschränkungen. Dieser Standardverbraucher muss von einem lokalen Mitglied der Gruppe Administratoren auf dem lokalen Computer konfiguriert werden. Wenn Sie ein Domänenkonto zum Erstellen des Abonnements verwenden, muss das LocalSystem-Konto über die erforderlichen Berechtigungen für die Domäne verfügen, um sicherzustellen, dass der Ersteller Mitglied der lokalen Administratorgruppe ist.
>
> [**CommandLineEventConsumer kann**](commandlineeventconsumer.md) nicht verwendet werden, um einen Prozess zu starten, der interaktiv ausgeführt wird.

 

Im folgenden Verfahren wird beschrieben, wie sie einen Ereignisverbraucher erstellen, der einen Prozess über eine Befehlszeile aus führt.

**So erstellen Sie einen Ereignisverbraucher, der einen Prozess über eine Befehlszeile aus führt**

1.  Erstellen Sie Managed Object Format (MOF)-Datei eine Instanz von [**CommandLineEventConsumer,**](commandlineeventconsumer.md) um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern. Weitere Informationen finden Sie unter [Entwerfen Managed Object Format -Klassen (MOF).](designing-managed-object-format--mof--classes.md)
2.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter,**](--eventfilter.md) und geben Sie ihr einen Namen.
3.  Erstellen Sie eine Abfrage, um den Ereignistyp anzugeben. Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)
4.  Erstellen Sie eine Instanz von [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) um den Filter der Instanz von [**CommandLineEventConsumer zu zuordnen.**](commandlineeventconsumer.md)
5.  Kompilieren Sie Ihre MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird eine neue Klasse namens "MyCmdLineConsumer" erstellt, um Ereignisse zu generieren, wenn eine Instanz der neuen Klasse am Ende einer MOF erstellt wird. Das Beispiel befindet sich im MOF-Code, aber Sie können die Instanzen programmgesteuert erstellen, indem Sie die [Skript-API](scripting-api-for-wmi.md) für WMI oder die [COM-API für WMI verwenden.](com-api-for-wmi.md)

Im folgenden Verfahren wird beschrieben, wie Sie eine neue Klasse namens MyCmdLineConsumer erstellen.

**So erstellen Sie eine neue Klasse namens MyCmdLineConsumer**

1.  Erstellen Sie die c: cmdlinetest.bat datei mit einem Befehl, der ein sichtbares Programm wie \\ \_ "calc.exe" ausricht.
2.  Kopieren Sie die MOF-Datei in eine Textdatei, und speichern Sie sie mit der Erweiterung .mof.
3.  Kompilieren Befehlsfenster MOF-Datei in einer Datei mit dem folgenden Befehl: **Mofcomp-Dateiname.mof**.

> [!Note]  
> Das in cmdline angegebene Programmtest.bat \_ ausgeführt werden.

 

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

[Überwachen und Reagieren auf Ereignisse mit Standardverbrauchern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
