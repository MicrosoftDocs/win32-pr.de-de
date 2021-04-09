---
description: Der Standardconsumer, der von der activescripteventconsumer-Klasse implementiert wird, ermöglicht einem Computer das Ausführen eines Skripts und das Ausführen von Maßnahmen, wenn wichtige Ereignisse auftreten, um sicherzustellen, dass ein Computer automatisch Probleme erkennen und beheben kann.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Ausführen eines Skripts auf der Grundlage eines Ereignisses
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868132"
---
# <a name="running-a-script-based-on-an-event"></a>Ausführen eines Skripts auf der Grundlage eines Ereignisses

Der Standardconsumer, der von der [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse implementiert wird, ermöglicht einem Computer das Ausführen eines Skripts und das Ausführen von Maßnahmen, wenn wichtige Ereignisse auftreten, um sicherzustellen, dass ein Computer automatisch Probleme erkennen und beheben kann.

Dieser Consumer wird standardmäßig im Namespace des Stamm **\\ Abonnements** geladen.

Sie können die Leistung aller Instanzen von [**activescripteventconsumer**](activescripteventconsumer.md) auf einem System konfigurieren, indem Sie die Werte der **Timeout** -oder **maximumscripts** -Eigenschaft in einer einzelnen Instanz von [**scriptingstandardconsumersetting**](scriptingstandardconsumersetting.md)festlegen.

Das grundlegende Verfahren für die Verwendung von Standardconsumern ist immer identisch und befindet sich in [Überwachung und Reaktion auf Ereignisse mit Standard](monitoring-and-responding-to-events-with-standard-consumers.md)Consumern. Das folgende Verfahren, das der Basis Prozedur hinzugefügt wird, ist spezifisch für die [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Skript ausführt.

> [!Caution]  
> Die [**activescripteventconsumer**](activescripteventconsumer.md) -Klasse verfügt über besondere Sicherheitseinschränkungen. Dieser Standardconsumer muss von einem lokalen Mitglied der Gruppe "Administratoren" auf dem lokalen Computer konfiguriert werden. Wenn Sie ein Domänen Konto zum Erstellen des Abonnements verwenden, muss das LocalSystem-Konto über die erforderlichen Berechtigungen für die Domäne verfügen, um sicherzustellen, dass der Ersteller Mitglied der lokalen Administratoren Gruppe ist.

 

Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumer erstellt wird, der ein Skript ausführt.

**So erstellen Sie einen Ereignisconsumer, der ein Skript ausführt**

1.  Schreiben Sie das Skript, das ausgeführt wird, wenn ein Ereignis stattfindet.

    Sie können das Skript in einer beliebigen Sprache schreiben, aber stellen Sie sicher, dass eine Skript-Engine für die Sprache, die Sie auswählen, auf dem Computer installiert ist. Das Skript muss keine WMI-Skript Objekte verwenden.

    Nur ein Administrator kann einen skriptconsumer einrichten, und das Skript wird unter den LocalSystem-Anmelde Informationen ausgeführt, die dem Consumer mit Ausnahme des Netzwerk Zugriffs umfassende Funktionen bieten. Das Skript hat jedoch keinen Zugriff auf bestimmte Benutzer Anmeldedaten, z. b. Umgebungsvariablen und Netzwerkfreigaben.

2.  Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**activescripteventconsumer**](activescripteventconsumer.md) , um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern.

    Sie können den Text des Skripts in **ScriptText** einfügen, oder Sie können den Pfad und den Dateinamen des Skripts in **scriptfilename** angeben. Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).

3.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter**](--eventfilter.md), benennen Sie Sie, und erstellen Sie dann eine Abfrage, um den Ereignistyp anzugeben, der die Ausführung des Skripts auslöst.

    Weitere Informationen finden Sie unter [Abfragen mit WQL](querying-with-wql.md).

4.  Erstellen Sie eine Instanz von [**\_ \_ filtertoconsumerbinding**](--filtertoconsumerbinding.md) , um den Filter der [**activescripteventconsumer**](activescripteventconsumer.md)-Instanz zuzuordnen.
5.  Kompilieren Sie die MOF-Datei mit [**Mofcomp.exe**](mofcomp.md).

In den Beispielen im folgenden Abschnitt werden zwei Möglichkeiten zum Implementieren eines ereignisgesteuerten Skripts veranschaulicht. Im ersten Beispiel wird ein Skript verwendet, das in einer externen Datei definiert ist, und im zweiten Beispiel wird ein Skript verwendet, das in den MOF-Code integriert ist. Die Beispiele sind in MOF-Code, aber Sie können die Instanzen Programm gesteuert erstellen, indem Sie entweder die [Skript-API für WMI](scripting-api-for-wmi.md) oder die [com-API für WMI](com-api-for-wmi.md)verwenden.

## <a name="example-using-an-external-script"></a>Beispiel für die Verwendung eines externen Skripts

Im folgenden Verfahren wird beschrieben, wie das Beispiel für ein externes Skript verwendet wird.

**So verwenden Sie das externe Skript Beispiel**

1.  Erstellen Sie eine Datei mit dem Namen "c: \\Asec.vbs", und kopieren Sie dann das Skript in diesem Beispiel hinein.
2.  Kopieren Sie die MOF-Liste in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.
3.  Kompilieren Sie die MOF-Datei in einem Eingabe Aufforderungs Fenster mit dem folgenden Befehl.

    " **Mamacomp** *filename * * *. MOF* "*

4.  Führen Sie den Rechner aus, mit dem ein calc.exe Prozess erstellt wird. Warten Sie länger als fünf Sekunden, schließen Sie das Rechner Fenster, und suchen Sie dann im Verzeichnis "C:" \\ nach einer Datei mit dem Namen "ASEC. log".

    Der folgende Text ähnelt dem Text, der in der Datei "ASEC. log" enthalten ist.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

Das folgende VBScript-Codebeispiel zeigt das Skript, das aufgerufen wird, wenn ein Ereignis vom permanenten Consumer empfangen wird. Das **targetevent** -Objekt ist eine [**\_ \_ instancedeletionevent**](--instancedeletionevent.md) -Instanz, sodass Sie eine Eigenschaft mit dem Namen **TargetInstance** hat, die eine [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Instanz ist, die zum Auslösen des Ereignisses verwendet wird. Die **Win32- \_ Prozess** Klasse verfügt über die Eigenschaften **UserModeTime** und **kernelmodetime** , die in der vom Skript erstellten Protokolldatei abgelegt werden.


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



Im folgenden MOF-Codebeispiel wird das Skript aufgerufen, wenn ein Ereignis empfangen wird. Er erstellt den Filter, den Consumer und die Bindung zwischen diesen im Namespace des Stamm **\\ Abonnements** .

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a>Beispiel für die Verwendung von Inline Skript

Im folgenden Verfahren wird beschrieben, wie Sie das Beispiel für Inline Skripts verwenden.

**So verwenden Sie das Inline Skript Beispiel**

1.  Kopieren Sie die MOF-Liste in diesem Abschnitt in eine Textdatei, und speichern Sie Sie mit der Erweiterung MOF.
2.  Kompilieren Sie die MOF-Datei in einem Eingabe Aufforderungs Fenster mit dem folgenden Befehl.

    " **Mamacomp** *filename * * *. MOF* "*

Das folgende MOF-Codebeispiel erstellt den Filter, den Consumer und die Bindung zwischen Ihnen und enthält außerdem das Skript Inline.

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überwachen von und reagieren auf Ereignisse mit Standard Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
