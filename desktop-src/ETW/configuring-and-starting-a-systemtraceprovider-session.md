---
description: SystemTraceProvider ist ein Kernelanbieter mit vordefinierten Kernelereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Konfigurieren und Starten einer SystemTraceProvider-Sitzung
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386740"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="bc706-103">Konfigurieren und Starten einer SystemTraceProvider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="bc706-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="bc706-104">SystemTraceProvider ist ein Kernelanbieter mit vordefinierten Kernelereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="bc706-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="bc706-105">Unter Windows 7 und Windows Server 2008 R2 konnte SystemTraceProvider nur für die NT-Kernelprotokollierungssitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc706-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="bc706-106">Auf Windows 8, Windows Server 2012 und höher, kann SystemTraceProvider für bis zu acht Protokollierungssitzungen multiplexiert werden.</span><span class="sxs-lookup"><span data-stu-id="bc706-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="bc706-107">Die ersten beiden Slots für Protokollierungssitzungen sind für die NT-Kernelprotokollierung und die Circular Kernel Context Logger reserviert.</span><span class="sxs-lookup"><span data-stu-id="bc706-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="bc706-108">Weitere Informationen zur Verwendung der NT-Kernelprotokollierungssitzung als Ablaufverfolgungsanbieter finden Sie unter [Konfigurieren und Starten der NT-Kernelprotokollierungssitzung.](configuring-and-starting-the-nt-kernel-logger-session.md)</span><span class="sxs-lookup"><span data-stu-id="bc706-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="bc706-109">Auf Windows 10 SDK-Build 20348 und höher kann SystemTraceProvider über separate Systemanbieter konfiguriert werden, die mit [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) wie standardmäßige Ereignisablaufverfolgung für Windows-Ereignisanbieter gesteuert werden können.</span><span class="sxs-lookup"><span data-stu-id="bc706-109">On Windows 10 SDK build 20348 and later, the SystemTraceProvider can be configured via separate System Providers, which can be controlled with [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) like standard Event Tracing for Windows event providers.</span></span> <span data-ttu-id="bc706-110">Eine vollständige Liste der Systemanbieter, Schlüsselwörter und entsprechenden Legacyflags und -gruppen finden Sie unter [Systemanbieter.](system-providers.md)</span><span class="sxs-lookup"><span data-stu-id="bc706-110">For a full list of system providers, keywords, and corresponding legacy flags and groups, see [System Providers](system-providers.md)</span></span>

## <a name="enable-a-systemtraceprovider-session"></a><span data-ttu-id="bc706-111">Aktivieren einer SystemTraceProvider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="bc706-111">Enable a SystemTraceProvider session</span></span>

<span data-ttu-id="bc706-112">Führen Sie den folgenden Befehl aus, damit SystemTraceProvider eine andere Sitzung als die NT-Kernelprotokollierung starten kann:</span><span class="sxs-lookup"><span data-stu-id="bc706-112">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command:</span></span>

<span data-ttu-id="bc706-113">**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="bc706-113">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="bc706-114">Um systemTraceProvider programmgesteuert so zu aktivieren, dass eine andere Sitzung als die NT-Kernelprotokollierung gestartet wird, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="bc706-114">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="bc706-115">Definieren Sie einen namen für die private Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="bc706-115">Define a private logger name.</span></span>

    <span data-ttu-id="bc706-116">**\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**</span><span class="sxs-lookup"><span data-stu-id="bc706-116">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="bc706-117">Legen Sie auf dem Controller die folgenden Member der [**EVENT \_ TRACE \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) fest.</span><span class="sxs-lookup"><span data-stu-id="bc706-117">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="bc706-118">Legen Sie **LogFileMode** auf **EVENT TRACE SYSTEM \_ \_ \_ LOGGER \_ MODE** fest.</span><span class="sxs-lookup"><span data-stu-id="bc706-118">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="bc706-119">Legen Sie **LoggerName** anstelle von **KERNEL \_ LOGGER \_ NAME** auf private Protokollierung fest.</span><span class="sxs-lookup"><span data-stu-id="bc706-119">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="bc706-120">Stellen Sie sicher, dass der **Wnode.Guid-Member** der [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) nicht auf **SystemTraceControlGuid** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bc706-120">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="bc706-121">Sie müssen diesem Element eine neue **GUID** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="bc706-121">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="bc706-122">Legen Sie auf dem Consumer den **Member LoggerName** der [**EVENT TRACE \_ \_ LOGFILE-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) auf diese private Protokollierung fest.</span><span class="sxs-lookup"><span data-stu-id="bc706-122">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="bc706-123">Wenn Sie möchten, dass ein Nicht-Administratoren- oder Nicht-TCB-Prozess eine Profilerstellungs-Ablaufverfolgungssitzung mit systemTraceProvider im Auftrag von Anwendungen von Drittanbietern starten kann, müssen Sie dem Benutzerprofil berechtigungen gewähren und diesen Benutzer dann sowohl der **Sitzungs-GUID** (erstellt für die Protokollierungssitzung) als auch der **GUID** des Systemablaufverfolgungsanbieters hinzufügen, um den Systemablaufverfolgungsanbieter zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc706-123">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="bc706-124">Weitere Informationen finden Sie in der [**EventAccessControl-Funktion.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)</span><span class="sxs-lookup"><span data-stu-id="bc706-124">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bc706-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc706-125">Related topics</span></span>

[<span data-ttu-id="bc706-126">Konfigurieren und Starten einer privaten Protokollierungssitzung</span><span class="sxs-lookup"><span data-stu-id="bc706-126">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)

[<span data-ttu-id="bc706-127">Konfigurieren und Starten einer AutoLogger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="bc706-127">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)

[<span data-ttu-id="bc706-128">Konfigurieren und Starten einer Ereignisablaufverfolgungssitzung</span><span class="sxs-lookup"><span data-stu-id="bc706-128">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)

[<span data-ttu-id="bc706-129">Konfigurieren und Starten der NT-Kernelprotokollierungssitzung</span><span class="sxs-lookup"><span data-stu-id="bc706-129">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)

[<span data-ttu-id="bc706-130">Systemanbieter</span><span class="sxs-lookup"><span data-stu-id="bc706-130">System Providers</span></span>](system-providers.md)

[<span data-ttu-id="bc706-131">Aktualisieren einer Ereignisablaufverfolgungssitzung</span><span class="sxs-lookup"><span data-stu-id="bc706-131">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)

 

 
