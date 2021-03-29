---
description: Der systemtraceprovider ist ein Kernel Anbieter mit vordefinierten Kernel Ereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Konfigurieren und Starten einer systemtraceprovider-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977712"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a><span data-ttu-id="0d86c-103">Konfigurieren und Starten einer systemtraceprovider-Sitzung</span><span class="sxs-lookup"><span data-stu-id="0d86c-103">Configuring and Starting a SystemTraceProvider Session</span></span>

<span data-ttu-id="0d86c-104">Der systemtraceprovider ist ein Kernel Anbieter mit vordefinierten Kernel Ereignissen, die unter Windows 7, Windows Server 2008 R2 und höher unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0d86c-104">The SystemTraceProvider is a kernel provider with a predefined sets of kernel events supported on Windows 7, Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="0d86c-105">Unter Windows 7 und Windows Server 2008 R2 konnte der systemtraceprovider nur für die NT Kernel Logger-Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d86c-105">On Windows 7 and Windows Server 2008 R2, the SystemTraceProvider could only be used for the NT Kernel Logger session.</span></span>

<span data-ttu-id="0d86c-106">Unter Windows 8, Windows Server 2012 und höher kann der systemtraceprovider für bis zu 8 Protokollierungs Sitzungen multiplext werden.</span><span class="sxs-lookup"><span data-stu-id="0d86c-106">On Windows 8, Windows Server 2012, and later, the SystemTraceProvider can be multiplexed for up to 8 logger sessions.</span></span> <span data-ttu-id="0d86c-107">Die ersten beiden Slots für Protokollierungs Sitzungen sind für die NT-Kernel Protokollierung und die zirkuläre Kernel Kontext Protokollierung reserviert.</span><span class="sxs-lookup"><span data-stu-id="0d86c-107">The first two slots for logger sessions are reserved for the NT Kernel Logger and the Circular Kernel Context Logger .</span></span>

<span data-ttu-id="0d86c-108">Weitere Informationen zur Verwendung der NT Kernel Logger-Sitzung als Ablauf Verfolgungs Anbieter finden Sie unter [Konfigurieren und Starten der NT-Kernel](configuring-and-starting-the-nt-kernel-logger-session.md)Protokollierungs Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0d86c-108">For more information on using the NT Kernel Logger session as a trace provider, see [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).</span></span>

<span data-ttu-id="0d86c-109">Führen Sie den folgenden Befehl aus, um den systemtraceprovider zum Starten einer anderen Sitzung als der NT-Kernel Protokollierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0d86c-109">To enable the SystemTraceProvider to start a session other than the NT Kernel Logger, execute the following command.</span></span>

<span data-ttu-id="0d86c-110">**tracelog-Start MySession-f c: \\ Kernel1. ETL-EFLAG proc \_ Thread + Loader + cswitch**</span><span class="sxs-lookup"><span data-stu-id="0d86c-110">**tracelog -start MySession -f c:\\Kernel1.etl -eflag PROC\_THREAD+LOADER+CSWITCH**</span></span>

<span data-ttu-id="0d86c-111">Führen Sie die folgenden Schritte aus, um den systemtraceprovider Programm gesteuert zum Starten einer anderen Sitzung als der NT-Kernel Protokollierung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0d86c-111">To programmatically enable the SystemTraceProvider to start a session other than the NT Kernel Logger, use the following steps.</span></span>

-   <span data-ttu-id="0d86c-112">Definieren Sie einen Namen für die private Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="0d86c-112">Define a private logger name.</span></span>

    <span data-ttu-id="0d86c-113">**\#definieren Sie den Namen der privaten Protokollierung \_ \_ L "Some private Trace Session".**</span><span class="sxs-lookup"><span data-stu-id="0d86c-113">**\#define PRIVATE\_LOGGER\_NAME L”Some Private Trace Session”**</span></span>

-   <span data-ttu-id="0d86c-114">Legen Sie auf dem Controller die folgenden Member der [**\_ \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) Struktur der Ereignis Ablauf Verfolgung fest.</span><span class="sxs-lookup"><span data-stu-id="0d86c-114">At the controller, set the following members of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure.</span></span>

    <span data-ttu-id="0d86c-115">Legen Sie **logfilemode** auf **Ereignis Ablauf \_ Verfolgungs \_ System \_ \_**-Protokollierungs Modus fest.</span><span class="sxs-lookup"><span data-stu-id="0d86c-115">Set **LogFileMode** to **EVENT\_TRACE\_SYSTEM\_LOGGER\_MODE**.</span></span>

    <span data-ttu-id="0d86c-116">Legen Sie **Loggername** anstelle des **\_ \_ namens der Kernel** Protokollierung auf private Logger fest.</span><span class="sxs-lookup"><span data-stu-id="0d86c-116">Set **LoggerName** to private logger, instead of **KERNEL\_LOGGER\_NAME**.</span></span>

    <span data-ttu-id="0d86c-117">Stellen Sie sicher, dass das **wnode. GUID** -Element der Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) nicht auf **systemtracecontrolguid** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0d86c-117">Make sure the **Wnode.Guid** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure is not set to **SystemTraceControlGuid**.</span></span> <span data-ttu-id="0d86c-118">Sie müssen diesem Member eine neue **GUID** zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0d86c-118">You must assign a new **GUID** to this member.</span></span>

-   <span data-ttu-id="0d86c-119">Legen Sie auf dem Consumer den **Loggername** -Member der [**Ereignis Ablauf \_ Verfolgung \_ logfile**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) -Struktur auf diese private Protokollierung fest.</span><span class="sxs-lookup"><span data-stu-id="0d86c-119">At the consumer, set the **LoggerName** member of the [**EVENT\_TRACE\_LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) structure to this private logger.</span></span>

> [!Note]  
> <span data-ttu-id="0d86c-120">Wenn ein nicht-Administratoren-oder ein nicht-TCB-Prozess in der Lage sein soll, eine Profilerstellungs-Ablauf Verfolgungs Sitzung mithilfe von systemtraceprovider im Namen von Drittanbieter Anwendungen zu starten, müssen Sie dem Benutzerprofil Berechtigungen erteilen und diesen Benutzer dann sowohl der Sitzungs- **GUID** (für die Protokollierungs Sitzung erstellt) als auch der **GUID** des System Ablauf Verfolgungs Anbieters hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0d86c-120">If you want a non-administrators or a non-TCB process to be able to start a profiling trace session using the SystemTraceProvider on behalf of third party applications, then you need to grant the user profile privilege and then add this user to both the session **GUID** (created for the logger session) and the system trace provider **GUID** to enable the system trace provider.</span></span> <span data-ttu-id="0d86c-121">Weitere Informationen finden Sie in der [**eventaccesscontrol**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0d86c-121">For more information, see the [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0d86c-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d86c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d86c-123">Konfigurieren und Starten einer Sitzung für private Logger</span><span class="sxs-lookup"><span data-stu-id="0d86c-123">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[<span data-ttu-id="0d86c-124">Konfigurieren und Starten einer autologger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="0d86c-124">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[<span data-ttu-id="0d86c-125">Konfigurieren und Starten einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="0d86c-125">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[<span data-ttu-id="0d86c-126">Konfigurieren und Starten der NT Kernel Logger-Sitzung</span><span class="sxs-lookup"><span data-stu-id="0d86c-126">Configuring and Starting the NT Kernel Logger Session</span></span>](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[<span data-ttu-id="0d86c-127">Aktualisieren einer Ereignis Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="0d86c-127">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
