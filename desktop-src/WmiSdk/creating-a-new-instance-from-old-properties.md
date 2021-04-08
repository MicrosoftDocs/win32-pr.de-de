---
description: Eine joinansichts Klasse enthält Eigenschaften aus Quell Klassen Instanzen, die durch einen allgemeinen Eigenschafts Wert verbunden sind, z. b. Class1. Eigenschaft PROP1 = Klasse2. Prop2. Jede Instanz in einer joinansichts Klasse besteht aus Teilen verschiedener Klassen Instanzen.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Erstellen einer neuen Instanz aus alten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960615"
---
# <a name="creating-a-new-instance-from-old-properties"></a>Erstellen einer neuen Instanz aus alten Eigenschaften

Eine joinansichts Klasse enthält Eigenschaften aus Quell Klassen Instanzen, die durch einen allgemeinen Eigenschafts Wert verbunden sind, z. b. **Class1. Eigenschaft PROP1**  =  **Klasse2. Prop2**. Jede Instanz in einer joinansichts Klasse besteht aus Teilen verschiedener Klassen Instanzen.

Sie können eine Verknüpfungs Ansichts Klasse auf Ungleichheit von Eigenschafts Werten, wie z **. b. Class1. Eigenschaft PROP1**  <>  **Klasse2. Prop2** , basieren, wobei **Eigenschaft PROP1** und **Prop2** nicht derselben Eigenschaft in der Ansichts Klasse zugeordnet werden.

Eine Join-Ansichts Klasse ist hilfreich, wenn die gesuchten Informationen in separaten, aber verwandten Klassen enthalten sind. Wenn Sie z. b. Informationen zu einem Drucker und zur Druckerkonfiguration benötigen, können Sie eine joinansichts Klasse erstellen, die einige der Eigenschaften der [**Win32- \_ Drucker**](/windows/desktop/CIMWin32Prov/win32-printer) Klasse und einige der Eigenschaften der Win32- [**Klasse \_ printerconfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) enthält. Ohne den Ansichts Anbieter müssen Sie die Eigenschaften der separaten Instanzen abrufen und zusammenführen, um die benötigten Informationen zu erhalten.

Im folgenden Verfahren wird beschrieben, wie eine joinansichts Klasse erstellt wird.

**So erstellen Sie eine joinansichts Klasse**

1.  Beginnen Sie eine Klassendefinition mit dem [**joinon**](qualifiers-specific-to-the-view-provider.md) -Zeichen folgen Qualifizierer.

    Die Qualifizierer [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** und **Union** schließen sich gegenseitig aus.

2.  Filtern Sie ggf. die gewünschten Instanzen in der joinklasse, indem Sie den [**postjoinfilter**](postjoinfilter-qualifier.md) -Qualifizierer anwenden.

    Mit dem [**postjoinfilter**](postjoinfilter-qualifier.md) -Anbieter können Sie die Instanzen einer Ansichts Klasse auf Instanzen beschränken, die bestimmte Bedingungen erfüllen.

3.  Erstellen Sie die Abfragen, die Quell Instanzen der Ansichts Klasse mit dem [**viewsources**](viewsources-qualifier.md) -Qualifizierer definieren.
4.  Definieren Sie die Namen und Speicherorte der Namespaces, in denen sich die Quell Instanzen mit dem [**viewspaces**](viewspaces-qualifier.md) -Qualifizierer befinden.
5.  Definieren Sie die gewünschten Eigenschaften in einer joinansichts Klasse mit dem [**propertysources**](propertysources-qualifier.md) -Qualifizierer.

    Wenn der joinansicht basierend auf Gleichheit Eigenschaften hinzugefügt werden, müssen die beiden Quell Eigenschaften in einem [**propertysources**](propertysources-qualifier.md) -Qualifizierer zugeordnet werden.

    Das folgende Codebeispiel zeigt zwei Eigenschaften, die in einem **propertysources** -Qualifizierer zugeordnet sind.

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    Wenn Sie den [**hiddendefault-Qualifizierer**](qualifiers-specific-to-the-view-provider.md) verwenden, können Sie die Eigenschaften markieren, die zu einer Quell Klasse gehören.

Das folgende Codebeispiel zeigt eine Verknüpfungs Ansichts Klasse, die aus den System Monitor-Anbieter Klassen [**Win32 \_ perfrawdata \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) und dem [**Win32 \_ perfrawdata \_ perfproc- \_ Thread**](/previous-versions//aa394325(v=vs.85)) mit den Eigenschaften beider Klassen erstellt wurde, die von der **ProcessID-** Eigenschaft verknüpft sind.

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
