---
description: Mithilfe der SMTPEventConsumer-Klasse können Sie E-Mails an einen angegebenen Benutzer senden, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein Standardereignis-Consumer, der von WMI zur Verfügung steht.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Senden von E-Mails basierend auf einem Ereignis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcef0858f7022fcb36006f038b20dedc940da60ee6c61e0372f5a74663093a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860418"
---
# <a name="sending-email-based-on-an-event"></a>Senden von E-Mails basierend auf einem Ereignis

Mithilfe der [SMTPEventConsumer-Klasse](smtpeventconsumer.md) können Sie E-Mails an einen angegebenen Benutzer senden, wenn ein angegebenes Ereignis auftritt. Diese Klasse ist ein [Standardereignis-Consumer,](standard-consumer-classes.md) der von WMI zur Verfügung steht.

Die [SMTPEventConsumer-Klasse](smtpeventconsumer.md) erfordert die folgenden Bedingungen, um eine E-Mail-Nachricht als Reaktion auf ein Ereignis zu senden:

-   Die [SMTPEventConsumer-Klasse](smtpeventconsumer.md) muss in den richtigen Namespace kompiliert werden. Weitere Informationen finden Sie unter [Überwachen und Reagieren auf Ereignisse mit Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md)
-   Ein SMTP-Server muss im Netzwerk vorhanden sein.
-   Die E-Mail-Nachricht darf keine Anlage enthalten.
-   Die E-Mail-Nachricht muss in US-ASCII codiert sein.

Das grundlegende Verfahren für die Verwendung von Standard-Consumern ist immer identisch und befindet sich unter [Überwachung und Reagieren auf Ereignisse mit Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md) Die folgende Prozedur fügt der grundlegenden Prozedur hinzu: ist spezifisch für die [SMTPEventConsumer-Klasse.](smtpeventconsumer.md) und beschreibt, wie ein Ereignisverbraucher erstellt wird, der E-Mails sendet.

Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisverbraucher erstellen, der E-Mails sendet.

**So erstellen Sie einen Ereignisverbraucher, der E-Mails sendet**

1.  Installieren und registrieren Sie bei Bedarf die [SMTPEventConsumer-Klasse.](smtpeventconsumer.md)

    Die [SMTPEventConsumer-Klasse](smtpeventconsumer.md) wird \\ vom WMI-Setupprogramm in den Stammabonnementnamespace kompiliert.

2.  Identifizieren Sie das Ereignis, das Sie überwachen möchten, und erstellen Sie die Ereignisabfrage.

    Möglicherweise gibt es ein vorhandenes systeminternes Ereignis, das zum Überwachen Ihres Ereignisses verwendet. Die meisten systeminternen Ereignisse sind Änderungen an Klasseninstanzen im Namespace "root \\ cimv2" zugeordnet. Wenn Sie die Klassen im [WMI-Klassenverweis](wmi-classes.md) analysieren, können Sie wahrscheinlich eine Klasse finden, die das zu überwachende Ereignis identifiziert. Verwenden Sie beispielsweise die [**Win32 \_ LogicalDisk-Klasse,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) um Änderungen an einem Festplattenlaufwerk zu überwachen.

    Wenn keine systeminternen Ereignisse vorhanden sind, die verwenden, kann es einen extrinsischen Ereignisanbieter geben, der funktionieren kann. Verwenden Sie beispielsweise die [**RegistryTreeChangeEvent-Klasse**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) des Registrierungsanbieters, um Änderungen an der Systemregistrierung zu überwachen.

    Wenn keine Klasse vorhanden ist, die das zu überwachende Ereignis identifiziert, müssen Sie einen eigenen Ereignisanbieter erstellen und neue extrinsische Ereignisklassen definieren. Weitere Informationen finden Sie unter [Schreiben eines Ereignisanbieters.](writing-an-event-provider.md)

3.  Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [SMTPEventConsumer,](smtpeventconsumer.md) um Ereignisse zu empfangen.

    Verwenden Sie die Eigenschaften der -Instanz, um die E-Mail-Nachricht zu definieren, die gesendet werden soll, wenn ein Ereignis auftritt. Beispielsweise definiert die **ToLine-Eigenschaft** die E-Mail-Adresse und die **Message-Eigenschaft** den Text der E-Mail-Nachricht. Sie müssen die E-Mail-Adresse, den Betreff und den Text einer Nachricht definieren, aber eine E-Mail-Nachricht darf keine Anlage enthalten. Weitere Informationen finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](designing-managed-object-format--mof--classes.md)

4.  Erstellen Sie eine Ereignisabfrage, die die Ereignisse angibt, die Sie überwachen möchten.

    Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)

5.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter,**](--eventfilter.md) und speichern Sie Ihre Abfrage in der **Query-Eigenschaft.**

    Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)

6.  Erstellen Sie eine Instanz von [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) um den Filter und den Consumer zuzuordnen.
7.  Kompilieren Sie die MOF-Datei [**mit**](mofcomp.md)Mofcomp.exe.


## <a name="example"></a>Beispiel

Das Beispiel in diesem Abschnitt befindet sich im MOF-Code. Sie können die Instanzen jedoch programmgesteuert erstellen, indem Sie die [Skript-API für WMI](scripting-api-for-wmi.md) oder die [COM-API für WMI](com-api-for-wmi.md)verwenden.

Im folgenden Verfahren wird die Verwendung des Beispiels beschrieben.

**So verwenden Sie das Beispiel**

1.  Kopieren Sie die folgende MOF-Datei in eine Textdatei, und speichern Sie sie mit der Erweiterung MOF.
2.  Kompilieren Sie die MOF-Datei in einem Eingabeaufforderungsfenster mit dem folgenden Befehl:

     *Mofcomp-Dateiname}.mof**

> [!Note]  
> Wenn MOF-Code in den \\ Stammabonnementnamespace kompiliert wird, wird [SMTPEventConsumer](smtpeventconsumer.md) in den gleichen Namespace kompiliert.

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen und Reagieren auf Ereignisse mit Standard-Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
