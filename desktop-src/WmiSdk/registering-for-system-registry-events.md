---
description: Zum Empfangen von Benachrichtigungen vom System Registrierungs Anbieter muss eine Verwaltungs Anwendung als temporärer Ereignisconsumer registriert werden.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrierung für System Registrierungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369055"
---
# <a name="registering-for-system-registry-events"></a><span data-ttu-id="a949a-103">Registrierung für System Registrierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="a949a-103">Registering for System Registry Events</span></span>

<span data-ttu-id="a949a-104">Zum Empfangen von Benachrichtigungen vom [System Registrierungs](/previous-versions/windows/desktop/regprov/system-registry-provider) Anbieter muss eine Verwaltungs Anwendung als temporärer Ereignisconsumer registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a949a-104">To receive notifications from the [System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider) provider, a management application must register as a temporary event consumer.</span></span> <span data-ttu-id="a949a-105">Die meisten Anforderungen für die Registrierung für den System Registrierungs Anbieter sind identisch mit allen anderen Ereignis Registrierungen, mit dem Unterschied, dass Sie auch das folgende Verfahren ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="a949a-105">Most of the requirements to register for the System Registry provider are the same as any other event registration, except you must also perform the following procedure.</span></span>

<span data-ttu-id="a949a-106">Der Registrierungs Anbieter stellt Ereignis Klassen für Ereignisse in der Systemregistrierung bereit.</span><span class="sxs-lookup"><span data-stu-id="a949a-106">The registry provider supplies event classes for events in the system registry.</span></span> <span data-ttu-id="a949a-107">Weitere Informationen zur allgemeinen Ereignis Registrierung finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="a949a-107">For more information about general event registration, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="a949a-108">Im folgenden Verfahren wird beschrieben, wie Sie sich für System Registrierungs Ereignisse registrieren.</span><span class="sxs-lookup"><span data-stu-id="a949a-108">The following procedure describes how to register for system registry events.</span></span>

<span data-ttu-id="a949a-109">**So registrieren Sie sich für System Registrierungs Ereignisse**</span><span class="sxs-lookup"><span data-stu-id="a949a-109">**To register for system registry events**</span></span>

1.  <span data-ttu-id="a949a-110">Ruft eine Benachrichtigungs Abfrage Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a949a-110">Call a notification query method.</span></span>

    <span data-ttu-id="a949a-111">Verwenden Sie entweder in Skript oder C++ eine Benachrichtigungs Abfrage, z. b. [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md) oder [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span><span class="sxs-lookup"><span data-stu-id="a949a-111">In either script or C++, use a notification query such as [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span></span> <span data-ttu-id="a949a-112">Erstellen Sie eine Abfrage Zeichenfolge für den *bstrinquery* -Parameter von **IWbemServices:: ExecNotificationQueryAsync** oder die ""- *Abfrage* "im Skript.</span><span class="sxs-lookup"><span data-stu-id="a949a-112">Create a query string for the *bstrQuery* parameter of **IWbemServices::ExecNotificationQueryAsync** or the *strQuery* in script.</span></span>

2.  <span data-ttu-id="a949a-113">Bestimmen Sie, welche Art von Ereignis Sie empfangen möchten, und erstellen Sie die Abfrage.</span><span class="sxs-lookup"><span data-stu-id="a949a-113">Determine which type of event you want to receive and create the query.</span></span>

    <span data-ttu-id="a949a-114">In der folgenden Tabelle sind die Registrierungs Ereignis Klassen aufgelistet, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a949a-114">The following table lists the registry event classes that you can use.</span></span>

    

    | <span data-ttu-id="a949a-115">Ereignisklasse</span><span class="sxs-lookup"><span data-stu-id="a949a-115">Event class</span></span>                                                      | <span data-ttu-id="a949a-116">Hive-Speicherort</span><span class="sxs-lookup"><span data-stu-id="a949a-116">Hive location</span></span>        | <span data-ttu-id="a949a-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a949a-117">Description</span></span>                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [<span data-ttu-id="a949a-118">**Registryevent**</span><span class="sxs-lookup"><span data-stu-id="a949a-118">**RegistryEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryevent)                       | <span data-ttu-id="a949a-119">–</span><span class="sxs-lookup"><span data-stu-id="a949a-119">N/A</span></span><br/>       | <span data-ttu-id="a949a-120">Abstrakte Basisklasse für Änderungen in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a949a-120">Abstract base class for changes in the registry.</span></span><br/> |
    | [<span data-ttu-id="a949a-121">**RegistryTreeChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="a949a-121">**RegistryTreeChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | <span data-ttu-id="a949a-122">RootPath</span><span class="sxs-lookup"><span data-stu-id="a949a-122">RootPath</span></span><br/>  | <span data-ttu-id="a949a-123">Überwacht Änderungen an einer Hierarchie von Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="a949a-123">Monitors changes to a hierarchy of keys.</span></span><br/>         |
    | [<span data-ttu-id="a949a-124">**RegistryKeyChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="a949a-124">**RegistryKeyChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | <span data-ttu-id="a949a-125">KEYPATH</span><span class="sxs-lookup"><span data-stu-id="a949a-125">KeyPath</span></span><br/>   | <span data-ttu-id="a949a-126">Überwacht Änderungen an einem einzelnen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="a949a-126">Monitors changes to a single key.</span></span><br/>                |
    | [<span data-ttu-id="a949a-127">**RegistryValueChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="a949a-127">**RegistryValueChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | <span data-ttu-id="a949a-128">ValueName</span><span class="sxs-lookup"><span data-stu-id="a949a-128">ValueName</span></span><br/> | <span data-ttu-id="a949a-129">Überwacht Änderungen an einem einzelnen Wert.</span><span class="sxs-lookup"><span data-stu-id="a949a-129">Monitors changes to a single value.</span></span><br/>              |

    

     

    <span data-ttu-id="a949a-130">Diese Klassen verfügen über eine Eigenschaft namens **Hive** , die die Hierarchie von Schlüsseln identifiziert, die auf Änderungen überwacht werden sollen, z. b. **HKEY \_ local \_ Machine**.</span><span class="sxs-lookup"><span data-stu-id="a949a-130">These classes have a property called **Hive** that identifies the hierarchy of keys to be monitored for change, such as **HKEY\_LOCAL\_MACHINE**.</span></span>

    <span data-ttu-id="a949a-131">Änderungen an den **HKEY \_ - \_ Klassen root** und **HKEY \_ Current \_ User** -Strukturen werden von [**registryevent**](/previous-versions/windows/desktop/regprov/registryevent) oder von ihr abgeleiteten Klassen, z. b. [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a949a-131">Changes to the **HKEY\_CLASSES\_ROOT** and **HKEY\_CURRENT\_USER** hives are not supported by [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) or classes derived from it, such as [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span></span>

3.  <span data-ttu-id="a949a-132">Erstellen Sie die WHERE-Klausel für die Ereignis Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a949a-132">Create the WHERE clause for your event registration.</span></span>

    <span data-ttu-id="a949a-133">Der System Registrierungs Anbieter verfügt über bestimmte Regeln für WHERE-Klauseln.</span><span class="sxs-lookup"><span data-stu-id="a949a-133">The System Registry provider has specific rules for WHERE clauses.</span></span> <span data-ttu-id="a949a-134">Weitere Informationen finden Sie unter [Erstellen einer richtigen WHERE-Klausel für den Registrierungs Anbieter](creating-a-proper-where-clause-for-the-registry-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a949a-134">For more information, see [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md).</span></span> <span data-ttu-id="a949a-135">Allgemeine Informationen zum Erstellen einer WHERE-Klausel finden Sie unter [Querying with WQL (Abfragen mit WQL](querying-with-wql.md)).</span><span class="sxs-lookup"><span data-stu-id="a949a-135">For more general information about creating a WHERE clause, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="a949a-136">Bestimmen Sie, ob Ihr Consumer Ereignisse empfängt.</span><span class="sxs-lookup"><span data-stu-id="a949a-136">Determine whether your consumer is receiving events.</span></span>

    <span data-ttu-id="a949a-137">Der System Registrierungs Anbieter garantiert nicht, dass alle gesendeten Ereignisse übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a949a-137">The System Registry provider does not guarantee that all sent events are delivered.</span></span> <span data-ttu-id="a949a-138">Weitere Informationen finden Sie unter [empfangen von Registrierungs Ereignissen](receiving-registry-events.md).</span><span class="sxs-lookup"><span data-stu-id="a949a-138">For more information, see [Receiving Registry Events](receiving-registry-events.md).</span></span>

<span data-ttu-id="a949a-139">Im folgenden VBScript-Codebeispiel wird gezeigt, wie eine Registrierungs Änderung in der HKEY-Software für **\_ lokale \_ Computer** \\  \\ **Microsoft** Hive oder Unterstruktur erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="a949a-139">The following VBScript code example shows how to detect a registry change in the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft** hive or subtree.</span></span> <span data-ttu-id="a949a-140">Dabei handelt es sich um ein Überwachungs Skript, das zu Demonstrationszwecken in einem Prozess mit dem Namen Wscript.exe ausgeführt wird, bis er im **Task-Manager** beendet, WMI beendet oder das Betriebssystem neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a949a-140">This is a monitoring script that, for demonstration purposes, runs in a process named Wscript.exe until it is terminated in **Task Manager**, WMI is stopped, or the operating system is rebooted.</span></span> <span data-ttu-id="a949a-141">Das Skript verwendet einen [*semisynchronen*](gloss-s.md) Aufruf von [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="a949a-141">The script uses a [*semisynchronous*](gloss-s.md) call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="a949a-142">Weitere Informationen zu semisynchronen aufrufen finden Sie unter [Erstellen eines semisynchronen Aufrufs mit VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a949a-142">For more information about semisynchronous calls, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



Im folgenden VBScript-Codebeispiel wird veranschaulicht, wie Sie die Änderung der Werte eines Schlüssels überwachen, indem Sie für den Registrierungs Anbieter-Ereignistyp [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)registrieren. Das Skript ruft eine asynchrone Methode auf, [**SWbemServices.Execnotificationqueryasync**](swbemservices-execnotificationqueryasync.md). <span data-ttu-id="a949a-145">Weitere Informationen zu asynchronen Aufrufen und zur Sicherheit finden Sie unter [Erstellen eines asynchronen Aufrufs mit VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="a949a-145">For more information about asynchronous calls and security, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="a949a-146">Das folgende Skript wird unbegrenzt ausgeführt, bis der Computer neu gestartet, WMI beendet oder das Skript beendet wird.</span><span class="sxs-lookup"><span data-stu-id="a949a-146">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="a949a-147">Um das Skript manuell anzuhalten, verwenden Sie den Task-Manager, um den Prozess zu unterbinden.</span><span class="sxs-lookup"><span data-stu-id="a949a-147">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="a949a-148">Verwenden Sie zum programmgesteuerten beenden die Methode " [**Beenden**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) " in der Win32- \_ Prozess Klasse.</span><span class="sxs-lookup"><span data-stu-id="a949a-148">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

