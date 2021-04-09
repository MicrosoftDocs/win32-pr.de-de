---
title: Überwachen von Sitzungs Verbindungen und verbindungsverbindungen
description: Um eine Anwendung bei Remotedesktopdienste zu registrieren, speichern Sie den Namen der virtuellen Kanal Serveranwendung in der Registrierung, indem Sie einen Unterschlüssel hinzufügen.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039094"
---
# <a name="monitoring-session-connections-and-disconnections"></a><span data-ttu-id="04527-103">Überwachen von Sitzungs Verbindungen und verbindungsverbindungen</span><span class="sxs-lookup"><span data-stu-id="04527-103">Monitoring session connections and disconnections</span></span>

<span data-ttu-id="04527-104">Für eine-Dienst Anwendung, z. b. eine Virtual Channel-Serveranwendung, um Sitzungs Verbindungen und-Verbindungen zu überwachen, müssen Sie Sie bei Remotedesktopdienste registrieren.</span><span class="sxs-lookup"><span data-stu-id="04527-104">For a service application, such as a virtual channel server application, to monitor session connections and disconnections, you must register it with Remote Desktop Services.</span></span> <span data-ttu-id="04527-105">Wenn Sie die Anwendung bei Remotedesktopdienste registrieren möchten, speichern Sie den Namen der Virtual Channel-Serveranwendung in der Registrierung, indem Sie einen Unterschlüssel unter folgendem Speicherort hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="04527-105">To register the application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="04527-106">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminalserver** \\ **AddIns**</span><span class="sxs-lookup"><span data-stu-id="04527-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**</span></span>

<span data-ttu-id="04527-107">Der Unterschlüssel kann einen beliebigen Namen haben.</span><span class="sxs-lookup"><span data-stu-id="04527-107">The subkey can have any name.</span></span> <span data-ttu-id="04527-108">Er muss über einen **reg \_ SZ** -Wert **namens** verfügen, der den symbolischen Namen der Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="04527-108">It must have a **REG\_SZ** value, **Name**, that contains the symbolic name of the application.</span></span>

``` syntax
Name = AddinName
```

<span data-ttu-id="04527-109">Die maximale Länge des unter Schlüssels und des Werts von **Name** beträgt 99 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="04527-109">The maximum length of both the subkey and the value of **Name** is 99 characters.</span></span>

<span data-ttu-id="04527-110">Der Unterschlüssel muss auch über einen **reg \_ DWORD** -Wert verfügen, der den Typ der Serveranwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="04527-110">The subkey must also have a **REG\_DWORD** value that indicates the type of server application.</span></span>

``` syntax
Type = AddinType
```

<span data-ttu-id="04527-111">*Addintype* muss den folgenden Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="04527-111">*AddinType* must be the following value.</span></span>



| <span data-ttu-id="04527-112">Wert</span><span class="sxs-lookup"><span data-stu-id="04527-112">Value</span></span> | <span data-ttu-id="04527-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="04527-113">Meaning</span></span>                               |
|-------|---------------------------------------|
| <span data-ttu-id="04527-114">3</span><span class="sxs-lookup"><span data-stu-id="04527-114">3</span></span>     | <span data-ttu-id="04527-115">Benutzermodusanwendung, Sitzungs Bereich.</span><span class="sxs-lookup"><span data-stu-id="04527-115">User-mode application, session space.</span></span> |



 

<span data-ttu-id="04527-116">Die Registrierung der-Dienst Anwendung wird nur in Sitzungen wirksam, die nach der Registrierung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="04527-116">Registration of the service application takes effect only in sessions created after the registration was performed.</span></span>

<span data-ttu-id="04527-117">Für jede registrierte Dienst Anwendung signalisiert Remotedesktopdienste einen Satz von Ereignis Objekten, wenn ein Client eine Verbindung mit der Sitzung herstellt oder diese trennt.</span><span class="sxs-lookup"><span data-stu-id="04527-117">For each registered service application, Remote Desktop Services will signal a set of event objects when a client connects or disconnects from the session.</span></span> <span data-ttu-id="04527-118">Jedes virtuelle Channel-Plug-in muss sich selbst registrieren und die Benachrichtigungs Ereignisse erstellen, indem [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="04527-118">Each virtual channel plug-in must register itself and create the notification events by calling [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span></span> <span data-ttu-id="04527-119">Die Namen dieser Ereignis Objekte entsprechen dem folgenden Format.</span><span class="sxs-lookup"><span data-stu-id="04527-119">The names of these event objects adhere to the following format.</span></span>

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

<span data-ttu-id="04527-120">*AddInName* ist die Zeichenfolge, die im **Name** -Wert des Registrierungs unter Schlüssels angegeben ist, unter dem die Serveranwendung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="04527-120">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="04527-121">Das Erstellen dieser Ereignisse in einer Sitzung bewirkt, dass Sie in einem speziellen Ereignis Verzeichnis pro Sitzung erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="04527-121">Creating these events under a session causes them to be created in a special per-session event directory.</span></span> <span data-ttu-id="04527-122">Das Ereignis Verzeichnis stellt zusätzliche Sicherheit bereit, indem verhindert wird, dass Anwendungen in anderen Sitzungen den Zustand dieser Ereignisse ändern.</span><span class="sxs-lookup"><span data-stu-id="04527-122">The event directory provides added security by preventing applications in other sessions from modifying the state of these events.</span></span>

<span data-ttu-id="04527-123">Um zu steuern, ob Verbindungs-und Trennungs Ereignisse auf dem Server empfangen werden, können Sie das Flag " **remotecontrolpersistent** " in der Registrierung unter folgendem Schlüssel platzieren:</span><span class="sxs-lookup"><span data-stu-id="04527-123">To control whether RECONNECT and DISCONNECT events are received on the server, you can place the **RemoteControlPersistent** flag in the registry under the following key:</span></span>

<span data-ttu-id="04527-124">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminalserver** \\ **AddIns** \\ *AddInName*</span><span class="sxs-lookup"><span data-stu-id="04527-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**\\*addinname*</span></span>

<span data-ttu-id="04527-125">Das Flag aktiviert oder deaktiviert das erneute Verbinden und trennen von Ereignissen, wenn eine Client Sitzung gestartet oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="04527-125">The flag enables or disables RECONNECT and DISCONNECT events from being signaled when a client session starts or stops.</span></span> <span data-ttu-id="04527-126">Die Syntax des **reg \_ DWORD** -Werts lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="04527-126">The syntax of the **REG\_DWORD** value is the following.</span></span>

``` syntax
RemoteControlPersistent = flag
```

<span data-ttu-id="04527-127">Der Wert des *Flags* kann ein oder NULL sein.</span><span class="sxs-lookup"><span data-stu-id="04527-127">The value of *flag* can be one or zero.</span></span> <span data-ttu-id="04527-128">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="04527-128">Zero is the default value.</span></span> <span data-ttu-id="04527-129">Wenn diese Einstellung auf 1 festgelegt ist, wird die Dienst Anwendung nicht benachrichtigt, wenn die Client Sitzung gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="04527-129">If set to one, the service application will not be notified if the client session is started or stopped.</span></span> <span data-ttu-id="04527-130">Wenn der Wert auf 0 (null) festgelegt ist, wird beim Starten der Client Sitzung ein Ereignis zum erneuten Verbinden signalisiert, und beim Anhalten der Client Sitzung wird ein Disconnect-Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="04527-130">If set to zero, a RECONNECT event is signaled when the client session starts, and a DISCONNECT event is signaled when the client session stops.</span></span>

<span data-ttu-id="04527-131">Das vorherige Ereignis Objekt Namensformat wird in Windows Server 2008 weiterhin aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04527-131">The previous event-object name format is still supported in Windows Server 2008 for backward compatibility.</span></span> <span data-ttu-id="04527-132">Es wird empfohlen, dass Sie das neuere Windows Server 2008-Format verwenden, da es sicherer ist.</span><span class="sxs-lookup"><span data-stu-id="04527-132">It is recommended that you use the newer Windows Server 2008 format because it is more secure.</span></span>

<span data-ttu-id="04527-133">Das vorherige Ereignis Format lautet wie folgt.</span><span class="sxs-lookup"><span data-stu-id="04527-133">The previous event format is as follows.</span></span>

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

<span data-ttu-id="04527-134">*AddInName* ist die Zeichenfolge, die im **Name** -Wert des Registrierungs unter Schlüssels angegeben ist, unter dem die Serveranwendung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="04527-134">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="04527-135">*SessionID* ist der Sitzungs Bezeichner einer Client Sitzung.</span><span class="sxs-lookup"><span data-stu-id="04527-135">*SessionId* is the session identifier of a client session.</span></span>

 

 