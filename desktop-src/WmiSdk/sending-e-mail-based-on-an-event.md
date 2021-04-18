---
description: Mithilfe der Klasse smtpeer-Consumer können Sie eine e-Mail an einen bestimmten Benutzer senden, wenn ein bestimmtes Ereignis eintritt. Diese Klasse ist ein Standard Ereignisconsumer, den WMI bereitstellt.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Senden von e-Mails auf der Grundlage eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358514"
---
# <a name="sending-email-based-on-an-event"></a>Senden von e-Mails auf der Grundlage eines Ereignisses

Mithilfe der Klasse [smtpeer-Consumer](smtpeventconsumer.md) können Sie eine e-Mail an einen bestimmten Benutzer senden, wenn ein bestimmtes Ereignis eintritt. Diese Klasse ist ein [Standard Ereignisconsumer](standard-consumer-classes.md) , den WMI bereitstellt.

Die Klasse [smtpventconsumer](smtpeventconsumer.md) erfordert die folgenden Bedingungen, um eine e-Mail-Nachricht als Antwort auf ein Ereignis zu senden:

-   Die Klasse [smtpeer-Consumer](smtpeventconsumer.md) muss in den richtigen Namespace kompiliert werden. Weitere Informationen finden Sie unter über [wachen und reagieren auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern.
-   Ein SMTP-Server muss im Netzwerk vorhanden sein.
-   Die e-Mail-Nachricht darf keine Anlage enthalten.
-   Die e-Mail-Nachricht muss in US-ASCII codiert werden.

Das grundlegende Verfahren für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern. Das folgende Verfahren fügt dem grundlegenden Verfahren hinzu. ist spezifisch für die Klasse [smtpeer Event Consumer](smtpeventconsumer.md) . und beschreibt, wie ein Ereignisconsumer erstellt wird, der eine e-Mail sendet.

Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumer erstellt wird, der eine e-Mail sendet.

**So erstellen Sie einen Ereignisconsumer, der eine e-Mail sendet**

1.  Installieren und registrieren Sie ggf. die Klasse [smtpventconsumer](smtpeventconsumer.md) .

    Die Klasse [smtpventconsumer](smtpeventconsumer.md) wird \\ vom WMI-Setup Programm in den Namespace des Stamm Abonnements kompiliert.

2.  Identifizieren Sie das Ereignis, das Sie überwachen möchten, und erstellen Sie die Ereignis Abfrage.

    Möglicherweise ist ein System internes Ereignis vorhanden, das zum Überwachen Ihres Ereignisses verwendet. Die meisten systeminternen Ereignisse werden Änderungen an Klassen Instanzen im \\ Namespace "root cimv2" zugeordnet. Wenn Sie die Klassen in der [WMI-Klassen](wmi-classes.md) Referenz analysieren, finden Sie wahrscheinlich eine Klasse, die das Ereignis identifiziert, das Sie überwachen möchten. Verwenden Sie z. b. die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse, um Änderungen an einem Festplattenlaufwerk zu überwachen.

    Wenn keine systeminternen Ereignisse vorhanden sind, die verwenden, kann möglicherweise ein System externe-Ereignis Anbieter funktionieren. Verwenden Sie z. b. die [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) -Klasse des Registrierungs Anbieters, um Änderungen an der Systemregistrierung zu überwachen.

    Wenn keine Klasse vorhanden ist, die das Ereignis identifiziert, das Sie überwachen möchten, müssen Sie einen eigenen Ereignis Anbieter erstellen und neue System externe-Ereignis Klassen definieren. Weitere Informationen finden Sie unter [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).

3.  Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [smtpeer-Consumer](smtpeventconsumer.md) , um Ereignisse zu empfangen.

    Verwenden Sie die Eigenschaften der-Instanz, um die e-Mail-Nachricht zu definieren, die bei einem Ereignis gesendet wird. Die **Toline** -Eigenschaft definiert z. b. die e-Mail-Adresse, und die **Message** -Eigenschaft definiert den Text der e-Mail-Nachricht. Sie müssen die e-Mail-Adresse, den Betreff und den Text einer Nachricht definieren, aber eine e-Mail-Nachricht kann keine Anlage enthalten. Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).

4.  Erstellen Sie eine Ereignis Abfrage, mit der die Ereignisse angegeben werden, die Sie überwachen möchten.

    Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).

5.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md) , und speichern Sie die Abfrage in der **Query** -Eigenschaft.

    Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).

6.  Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter und den Consumer zuzuordnen.
7.  Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).


## <a name="example"></a>Beispiel

Das Beispiel in diesem Abschnitt ist ein MOF-Code, aber Sie können die Instanzen Programm gesteuert mithilfe der [Skript-API für WMI](scripting-api-for-wmi.md) oder der [com-API für WMI](com-api-for-wmi.md)erstellen.

Im folgenden Verfahren wird beschrieben, wie das Beispiel verwendet wird.

**So verwenden Sie das Beispiel**

1.  Kopieren Sie die folgende MOF-Datei in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.
2.  Kompilieren Sie die MOF-Datei in einem Eingabe Aufforderungs Fenster mit dem folgenden Befehl:

    " **Mamacomp** *filename * * *. MOF* "*

> [!Note]  
> Wenn der MOF-Code in den Namespace des Stamm Abonnements kompiliert wird \\ , wird der [smtpeer-Consumer](smtpeventconsumer.md) in den gleichen Namespace kompiliert.

 

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

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
