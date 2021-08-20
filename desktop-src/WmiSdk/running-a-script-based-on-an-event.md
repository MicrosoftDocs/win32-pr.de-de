---
description: Der von der ActiveScriptEventConsumer-Klasse implementierte Standardconsumer ermöglicht einem Computer das Ausführen eines Skripts und das Ausführen von Maßnahmen, wenn wichtige Ereignisse auftreten, um sicherzustellen, dass ein Computer Probleme automatisch erkennen und beheben kann.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Ausführen eines Skripts basierend auf einem Ereignis
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b5950ae8a4e7260932fd4df559a73f3abea2bfaf7722444db0b92470649dd312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816738"
---
# <a name="running-a-script-based-on-an-event"></a>Ausführen eines Skripts basierend auf einem Ereignis

Der von der [**ActiveScriptEventConsumer-Klasse**](activescripteventconsumer.md) implementierte Standardconsumer ermöglicht einem Computer das Ausführen eines Skripts und das Ausführen von Maßnahmen, wenn wichtige Ereignisse auftreten, um sicherzustellen, dass ein Computer Probleme automatisch erkennen und beheben kann.

Dieser Consumer wird standardmäßig im **\\ Stammabonnementnamespace** geladen.

Sie können die Leistung aller Instanzen von [**ActiveScriptEventConsumer**](activescripteventconsumer.md) auf einem System konfigurieren, indem Sie die Werte der **Timeout-** oder **MaximumScripts-Eigenschaft** in einer einzelnen Instanz von [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)festlegen.

Das grundlegende Verfahren für die Verwendung von Standard-Consumern ist immer identisch und befindet sich unter [Überwachung und Reagieren auf Ereignisse mit Standard-Consumern.](monitoring-and-responding-to-events-with-standard-consumers.md) Die folgende Prozedur, die der grundlegenden Prozedur hinzufügt, ist spezifisch für die [**ActiveScriptEventConsumer-Klasse**](activescripteventconsumer.md) und beschreibt, wie ein Ereignisconsumer erstellt wird, der ein Skript ausführt.

> [!Caution]  
> Die [**ActiveScriptEventConsumer-Klasse**](activescripteventconsumer.md) weist spezielle Sicherheitseinschränkungen auf. Dieser Standardverbraucher muss von einem lokalen Mitglied der Gruppe Administratoren auf dem lokalen Computer konfiguriert werden. Wenn Sie ein Domänenkonto zum Erstellen des Abonnements verwenden, muss das LocalSystem-Konto über die erforderlichen Berechtigungen für die Domäne verfügen, um zu überprüfen, ob der Ersteller Mitglied der lokalen Administratorengruppe ist.

 

Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisverbraucher erstellen, der ein Skript ausführt.

**So erstellen Sie einen Ereignisverbraucher, der ein Skript ausführt**

1.  Schreiben Sie das Skript, das ausgeführt werden soll, wenn ein Ereignis stattfindet.

    Sie können das Skript in einer beliebigen Sprache schreiben, aber stellen Sie sicher, dass eine Skript-Engine für die sprache, die Sie auswählen, auf Ihrem Computer installiert ist. Das Skript muss keine WMI-Skriptobjekte verwenden.

    Nur ein Administrator kann einen Skript-Consumer einrichten, und das Skript wird unter LocalSystem-Anmeldeinformationen ausgeführt, was dem Consumer mit Ausnahme des Netzwerkzugriffs umfassende Funktionen bietet. Das Skript hat jedoch keinen Zugriff auf bestimmte Benutzeranmeldungsdaten, z. B. Umgebungsvariablen und Netzwerkfreigaben.

2.  Erstellen Sie in der MOF-Datei (Managed Object Format) eine Instanz von [**ActiveScriptEventConsumer,**](activescripteventconsumer.md) um die Ereignisse zu empfangen, die Sie in der Abfrage anfordern.

    Sie können den Text des Skripts in **ScriptText** speichern, oder Sie können den Pfad und den Dateinamen des Skripts in **ScriptFileName** angeben. Weitere Informationen finden Sie unter [Entwerfen von MOF-Klassen (Managed Object Format).](designing-managed-object-format--mof--classes.md)

3.  Erstellen Sie eine Instanz von [**\_ \_ EventFilter,**](--eventfilter.md)benennen Sie sie, und erstellen Sie dann eine Abfrage, um den Ereignistyp anzugeben, der die Ausführung des Skripts auslöst.

    Weitere Informationen finden Sie unter [Abfragen mit WQL.](querying-with-wql.md)

4.  Erstellen Sie eine Instanz von [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) um den Filter der Instanz von [**ActiveScriptEventConsumer**](activescripteventconsumer.md)zuzuordnen.
5.  Kompilieren Sie die MOF-Datei [**mit**](mofcomp.md)Mofcomp.exe.

Die Beispiele im folgenden Abschnitt zeigen zwei Möglichkeiten zum Implementieren eines ereignisgesteuerten Skripts. Im ersten Beispiel wird ein Skript verwendet, das in einer externen Datei definiert ist, und im zweiten Beispiel wird ein Skript verwendet, das in den MOF-Code integriert ist. Die Beispiele befinden sich im MOF-Code, aber Sie können die Instanzen programmgesteuert erstellen, indem Sie entweder die [Skript-API für WMI](scripting-api-for-wmi.md) oder die [COM-API für WMI](com-api-for-wmi.md)verwenden.

## <a name="example-using-an-external-script"></a>Beispiel für die Verwendung eines externen Skripts

Im folgenden Verfahren wird beschrieben, wie das externe Skriptbeispiel verwendet wird.

**So verwenden Sie das Beispiel für ein externes Skript**

1.  Erstellen Sie eine Datei mit dem Namen c: \\Asec.vbs, und kopieren Sie dann das Skript in diesem Beispiel hinein.
2.  Kopieren Sie die MOF-Liste in eine Textdatei, und speichern Sie sie mit der Erweiterung MOF.
3.  Kompilieren Sie die MOF-Datei in einem Eingabeaufforderungsfenster mit dem folgenden Befehl.

     *Mofcomp-Dateiname}.mof**

4.  Führen Sie den Rechner aus, um einen calc.exe Prozess zu erstellen. Warten Sie mehr als fünf Sekunden, schließen Sie das Fenster Rechner, und suchen Sie dann im Verzeichnis C: nach \\ einer Datei mit dem Namen ASEC.log.

    Der folgende Text ähnelt dem Text, der in der Datei ASEC.log enthalten ist.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

Das folgende VBScript-Codebeispiel zeigt das Skript, das aufgerufen wird, wenn ein Ereignis vom permanenten Consumer empfangen wird. Das **TargetEvent-Objekt** ist eine [**\_ \_ InstanceDeletionEvent-Instanz,**](--instancedeletionevent.md) sodass es über eine Eigenschaft namens **TargetInstance** verfügt, bei der es sich um eine [**Win32 \_ Process-Instanz**](/windows/desktop/CIMWin32Prov/win32-process) handelt, die zum Auslösen des Ereignisses verwendet wird. Die **Win32 \_ Process-Klasse** verfügt über die Eigenschaften **UserModeTime** und **KernelModeTime,** die in die vom Skript erstellte Protokolldatei aufgenommen werden.


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



Das folgende MOF-Codebeispiel ruft das Skript auf, wenn ein Ereignis empfangen wird. Er erstellt den Filter, den Consumer und die Bindung zwischen ihnen im **\\ Stammabonnementnamespace.**

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

## <a name="example-using-inline-script"></a>Beispiel für die Verwendung eines Inlineskripts

Das folgende Verfahren beschreibt die Verwendung des Inlineskriptbeispiels.

**So verwenden Sie das Inlineskriptbeispiel**

1.  Kopieren Sie die MOF-Liste in diesem Abschnitt in eine Textdatei, und speichern Sie sie mit der Erweiterung MOF.
2.  Kompilieren Sie die MOF-Datei in einem Eingabeaufforderungsfenster mit dem folgenden Befehl.

     *Mofcomp-Dateiname}.mof**

Im folgenden MOF-Codebeispiel werden der Filter, der Consumer und die Bindung zwischen ihnen erstellt, und es enthält auch das Skript inline.

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

[Überwachen und Reagieren auf Ereignisse mit Standard-Consumern](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
