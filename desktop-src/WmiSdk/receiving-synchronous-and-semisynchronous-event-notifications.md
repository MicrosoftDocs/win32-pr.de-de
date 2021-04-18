---
description: Verwenden Sie SWbemServices.Execquery, um alle vorhandenen Ereignisse anzufordern.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Empfangen synchroner und semisynchroner Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347681"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a><span data-ttu-id="292fa-103">Empfangen synchroner und semisynchroner Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="292fa-103">Receiving Synchronous and Semisynchronous Event Notifications</span></span>

<span data-ttu-id="292fa-104">Verwenden Sie [**SWbemServices.Execquery**](swbemservices-execquery.md) , um alle vorhandenen Ereignisse anzufordern.</span><span class="sxs-lookup"><span data-stu-id="292fa-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to request all existing events.</span></span>

<span data-ttu-id="292fa-105">Im folgenden Codebeispiel wird gezeigt, wie die Ereignisse in einem Protokoll abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="292fa-105">The following code example shows how to query for the events in a log.</span></span>

`Select * from Win32_NTLogEvent`

<span data-ttu-id="292fa-106">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md), [empfangen von Ereignis Benachrichtigungen](receiving-event-notifications.md)und [WQL (SQL für WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-106">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md), [Receiving Event Notifications](receiving-event-notifications.md), and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="292fa-107">Der Standard Aufruf von [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) verwendet die semisynchrone Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="292fa-107">The default call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) uses semisynchronous communication.</span></span> <span data-ttu-id="292fa-108">Der *IFlags* -Parameter verfügt über die standardmäßig festgelegten **wbemFlagForwardOnly** -und **wbemFlagReturnImmediately** -Flags.</span><span class="sxs-lookup"><span data-stu-id="292fa-108">The *iflags* parameter has the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags set by default.</span></span> <span data-ttu-id="292fa-109">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="292fa-110">Im folgenden Verfahren wird beschrieben, wie die semisynchrone Ereignis Benachrichtigung mithilfe von VBScript empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="292fa-110">The following procedure describes how to receive semisynchronous event notification using VBScript.</span></span>

<span data-ttu-id="292fa-111">**So empfangen Sie eine semisynchrone Ereignis Benachrichtigung in VBScript**</span><span class="sxs-lookup"><span data-stu-id="292fa-111">**To receive semisynchronous event notification in VBScript**</span></span>

1.  <span data-ttu-id="292fa-112">Erstellen Sie eine Abfrage für den Ereignistyp, den Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="292fa-112">Create a query for the type of event that you want to receive.</span></span> <span data-ttu-id="292fa-113">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-113">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="292fa-114">Wenn Sie einen Ereignistyp des Ereignisses (z. b. [**\_ \_ instancecreationevent**](--instancecreationevent.md)) anfordern, geben Sie in der Abfrage einen Typ der Ziel Instanz an, z. b. [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="292fa-114">If you request an instance type of event such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), indicate in the query a type of target instance, for example, [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>

3.  <span data-ttu-id="292fa-115">Geben Sie ggf. eine Instanz an, z. b. den Namen eines Namespace, wenn Sie zukünftige [**\_ \_ namespacemodificationevent**](--namespacemodificationevent.md) -Instanzen für einen bestimmten Namespace anfordern.</span><span class="sxs-lookup"><span data-stu-id="292fa-115">If necessary, specify an instance, for example, the name of a namespace when requesting future [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) instances for a specific namespace.</span></span>

4.  <span data-ttu-id="292fa-116">Geben Sie ein Abruf Intervall für Windows-Verwaltungsinstrumentation (WMI) in einer Abfrage an, z. b. "innerhalb 10" –, um alle 10 Sekunden eine Abfrage durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="292fa-116">Specify a polling interval for Windows Management Instrumentation (WMI) in a query, such as "WITHIN 10"—to poll every 10 seconds.</span></span> <span data-ttu-id="292fa-117">Weitere Informationen finden Sie unter [within-Klausel](within-clause.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-117">For more information, see [WITHIN Clause](within-clause.md).</span></span>

5.  <span data-ttu-id="292fa-118">Ruft [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md) mithilfe der Abfrage auf.</span><span class="sxs-lookup"><span data-stu-id="292fa-118">Call [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) using the query.</span></span>

6.  <span data-ttu-id="292fa-119">Durchlaufen Sie die Auflistung, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="292fa-119">Loop through the collection you receive.</span></span>

<span data-ttu-id="292fa-120">Im folgenden Beispiel wird gezeigt, wie Sie das Einfügen und Entfernen von Datenträgern von einem Diskettenlaufwerk auf einem lokalen Computer überwachen.</span><span class="sxs-lookup"><span data-stu-id="292fa-120">The following example shows how to monitor insertion and removal of disks from a floppy disk drive on a local machine.</span></span> <span data-ttu-id="292fa-121">Das Skript fordert \_ [**\_ \_ instancemodificationevent**](--instancemodificationevent.md) -Instanzen für die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanz des Disketten Laufwerks an und fragt alle 10 Sekunden nach neuen Instanzen ab.</span><span class="sxs-lookup"><span data-stu-id="292fa-121">The script requests \_[**\_\_InstanceModificationEvent**](--instancemodificationevent.md) instances for the floppy drive [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance and polls every 10 seconds for new instances.</span></span> <span data-ttu-id="292fa-122">Dieses Skript ist ein Beispiel für einen temporären Ereignisconsumer und wird weiter ausgeführt, bis er im Task-Manager angehalten oder das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="292fa-122">This script is an example of a temporary event consumer, and continues running until it is stopped in Task Manager or the system is rebooted.</span></span> <span data-ttu-id="292fa-123">Weitere Informationen finden Sie unter [empfangen von Ereignissen für die Dauer Ihrer Anwendung](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-123">For more information, see [Receiving Events for the Duration of your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



<span data-ttu-id="292fa-124">Im folgenden Verfahren wird beschrieben, wie Sie mit C++ semisynchrone Ereignis Benachrichtigungen empfangen.</span><span class="sxs-lookup"><span data-stu-id="292fa-124">The following procedure describes how to receive semisynchronous event notification using C++.</span></span>

<span data-ttu-id="292fa-125">**So empfangen Sie eine semisynchrone Ereignis Benachrichtigung in C++**</span><span class="sxs-lookup"><span data-stu-id="292fa-125">**To receive semisynchronous event notification in C++**</span></span>

1.  <span data-ttu-id="292fa-126">Richten Sie die Anwendung mit Aufrufen der Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein.</span><span class="sxs-lookup"><span data-stu-id="292fa-126">Set up the application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="292fa-127">Da WMI auf com basiert, ist der Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ein erforderlicher Schritt für eine WMI-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="292fa-127">Because WMI is COM based, calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a required step for a WMI application.</span></span> <span data-ttu-id="292fa-128">Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-128">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

2.  <span data-ttu-id="292fa-129">Bestimmen Sie die Art der Ereignisse, die Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="292fa-129">Determine the kind of events that you want to receive.</span></span>

    <span data-ttu-id="292fa-130">WMI unterstützt systeminterne und extrinsische Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="292fa-130">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="292fa-131">Ein System internes Ereignis ist ein von WMI vordefiniertes Ereignis.</span><span class="sxs-lookup"><span data-stu-id="292fa-131">An intrinsic event is an event predefined by WMI.</span></span> <span data-ttu-id="292fa-132">Ein System externe-Ereignis ist ein Ereignis, das von einem Drittanbieter definiert wird.</span><span class="sxs-lookup"><span data-stu-id="292fa-132">An extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="292fa-133">Weitere Informationen finden Sie unter [bestimmen des empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-133">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

3.  <span data-ttu-id="292fa-134">Registrieren Sie sich, um eine bestimmte Ereignisklasse mit einem Aufruf der [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) -Methode zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="292fa-134">Register to receive a specific class of events with a call to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) method.</span></span>

    <span data-ttu-id="292fa-135">Stellen Sie jede Abfrage sehr spezifisch dar.</span><span class="sxs-lookup"><span data-stu-id="292fa-135">Make each query very specific.</span></span> <span data-ttu-id="292fa-136">Das Ziel der Registrierung besteht darin, sich zu registrieren, um nur die erforderlichen Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="292fa-136">The goal of registration is to register to receive only the required notifications.</span></span> <span data-ttu-id="292fa-137">Benachrichtigungen, bei denen die Verarbeitungs-und Übermittlungs Zeit nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="292fa-137">Notifications that are not required waste processing and delivery time.</span></span>

    <span data-ttu-id="292fa-138">Sie können einen Ereignisconsumer so entwerfen, dass er mehrere Ereignisse empfängt.</span><span class="sxs-lookup"><span data-stu-id="292fa-138">You can design an event consumer to receive multiple events.</span></span> <span data-ttu-id="292fa-139">Beispielsweise kann ein Consumer eine Benachrichtigung über instanzänderungsereignisse für eine bestimmte Klasse von Geräte-und Sicherheits Verletzungs Ereignissen anfordern.</span><span class="sxs-lookup"><span data-stu-id="292fa-139">For example, a consumer might require notification of instance modification events for a specific class of device and security violation events.</span></span> <span data-ttu-id="292fa-140">In diesem Fall unterscheiden sich die Tasks, die ein Consumer beim Empfang eines instanzänderungsereignisses ausführt, für die beiden Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="292fa-140">In this case, the tasks a consumer performs when receiving an instance modification event are different for the two events.</span></span> <span data-ttu-id="292fa-141">Folglich sollte der Consumer einen Aufruf von [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) durchführen, um sich für instanzänderungsereignisse zu registrieren, und einen weiteren Aufruf von **ExecNotificationQuery** , um sich für Sicherheits Verletzungs Ereignisse zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="292fa-141">Thus, the consumer should make one call to [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) to register for instance modification events, and another call to **ExecNotificationQuery** to register for security violation events.</span></span>

    <span data-ttu-id="292fa-142">Legen Sie im Aufruf von [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)den *lFlags* -Parameter auf das **WBEM- \_ Flag \_ \_ sofort zurück** , und verwenden Sie das **WBEM- \_ Flag \_ \_ nur vorwärts**.</span><span class="sxs-lookup"><span data-stu-id="292fa-142">In the call to [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), set the *lFlags* parameter to **WBEM\_FLAG\_RETURN\_IMMEDIATELY** and **WBEM\_FLAG\_FORWARD\_ONLY**.</span></span> <span data-ttu-id="292fa-143">Das **WBEM- \_ Flag \_ gibt \_ sofort** die semisynchrone Verarbeitung von Flags zurück, und das Flag für das **WBEM-Flag " \_ \_ Vorwärts \_** " fordert einen vorwärts-Enumerator an.</span><span class="sxs-lookup"><span data-stu-id="292fa-143">The **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag requests semisynchronous processing, and the **WBEM\_FLAG\_FORWARD\_ONLY** flag requests a forward-only enumerator.</span></span> <span data-ttu-id="292fa-144">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="292fa-144">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="292fa-145">Die **ExecNotificationQuery** -Funktion gibt einen Zeiger auf eine [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="292fa-145">The **ExecNotificationQuery** function returns a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface.</span></span>

4.  <span data-ttu-id="292fa-146">Abrufen registrierter Ereignis Benachrichtigungen durch wiederholte Aufrufe der [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) -Methode.</span><span class="sxs-lookup"><span data-stu-id="292fa-146">Poll for registered event notifications by making repeated calls to the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span>
5.  <span data-ttu-id="292fa-147">Wenn Sie fertig sind, geben Sie den Enumerator frei, der auf das [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Objekt zeigt.</span><span class="sxs-lookup"><span data-stu-id="292fa-147">When finished, release the enumerator that points to the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object.</span></span>

    <span data-ttu-id="292fa-148">Sie können den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger freigeben, der der Registrierung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="292fa-148">You can release the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer associated with the registration.</span></span> <span data-ttu-id="292fa-149">Das Freigeben des **IWbemServices** -Zeigers bewirkt, dass WMI keine Ereignisse mehr an alle zugeordneten temporären Consumer übergibt.</span><span class="sxs-lookup"><span data-stu-id="292fa-149">Releasing the **IWbemServices** pointer causes WMI to stop delivering events to all associated temporary consumers.</span></span>

 

 
