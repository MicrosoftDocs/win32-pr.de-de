---
description: WinHTTP-Protokolle können verwendet werden, um die Problembehandlung von WSDAPI-Anwendungen zu unterstützen. Dies ist hilfreich, wenn der Metadatenaustausch fehlschlägt oder wenn die SSL/TLS-Aushandlung fehlschlägt.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Erfassen von WinHTTP-Protokollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131144"
---
# <a name="capturing-winhttp-logs"></a><span data-ttu-id="c4b5c-104">Erfassen von WinHTTP-Protokollen</span><span class="sxs-lookup"><span data-stu-id="c4b5c-104">Capturing WinHTTP Logs</span></span>

<span data-ttu-id="c4b5c-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) -Protokolle können verwendet werden, um die Problembehandlung von WSDAPI-Anwendungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-105">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logs can be used to help troubleshoot WSDAPI applications.</span></span> <span data-ttu-id="c4b5c-106">Dies ist hilfreich, wenn der Metadatenaustausch fehlschlägt oder wenn die SSL/TLS-Aushandlung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-106">This is helpful when metadata exchange fails or when SSL/TLS negotiation fails.</span></span>

<span data-ttu-id="c4b5c-107">In diesem Verfahren wird gezeigt, wie Sie WinHTTP-Protokolle auf dem Client-PC erfassen.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-107">This procedure shows how to capture WinHTTP logs on the client PC.</span></span> <span data-ttu-id="c4b5c-108">Die auf WSDAPI basierende Client Anwendung darf nicht ausgeführt werden, wenn die Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-108">The WSDAPI-based client application must not be running when logging is enabled.</span></span> <span data-ttu-id="c4b5c-109">Wenn die Client Anwendung ausgeführt wird, während die Protokollierung aktiviert ist, müssen der Client und/oder der PC neu gestartet werden, bevor WS-Discovery und Metadatenaustausch-Datenverkehr in den WinHTTP-Protokollen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-109">If the client application is running when logging is enabled, the client and/or the PC must be restarted before WS-Discovery and metadata exchange traffic will appear in the WinHTTP logs.</span></span>

<span data-ttu-id="c4b5c-110">**So erfassen Sie WinHTTP-Protokolle**</span><span class="sxs-lookup"><span data-stu-id="c4b5c-110">**To capture WinHTTP logs**</span></span>

1.  <span data-ttu-id="c4b5c-111">Öffnen Sie auf dem Client-PC ein Eingabe Aufforderungs Fenster mit erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-111">Open an elevated command prompt window on the client PC.</span></span>
2.  <span data-ttu-id="c4b5c-112">Führen Sie den folgenden Befehl aus: **netsh WinHTTP Set Tracing Trace-File-prefix = "C: \\ Temp \\ DPWS" Level = Verbose Format = ANSI State = aktivierte Max-Trace-File-size = 1073741824**</span><span class="sxs-lookup"><span data-stu-id="c4b5c-112">Run the following command: **netsh winhttp set tracing trace-file-prefix="C:\\Temp\\dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**</span></span>

    <span data-ttu-id="c4b5c-113">Dieser Befehl aktiviert die WinHTTP-Protokollierung.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-113">This command enables WinHTTP logging.</span></span> <span data-ttu-id="c4b5c-114">Alle Protokolldateien werden im Verzeichnis "C: Temp" gespeichert \\ , und die Dateinamen beginnen mit dem DPWS-Präfix.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-114">All log files will be stored in the C:\\Temp directory, and the filenames will begin with the dpws prefix.</span></span> <span data-ttu-id="c4b5c-115">Es werden höchstens 1 GB Protokolldateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-115">At most 1 GB of log files will be stored.</span></span>

3.  <span data-ttu-id="c4b5c-116">Wenn der Prozess, der auf dem Client mit WinHTTP ausgeführt wird, bereits ausgeführt wird, starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-116">If the process using WinHTTP on the client is already running, restart the computer.</span></span> <span data-ttu-id="c4b5c-117">Wenn z. b. die [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlungs-APIs verwendet werden, muss der Computer neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-117">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span> <span data-ttu-id="c4b5c-118">Von den funktionsermittlungs-APIs wird WinHTTP von innerhalb eines Dienst Hosts aufgerufen, der möglicherweise bereits gestartet wurde, als die Ablauf Verfolgung aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-118">The Function Discovery APIs call WinHTTP from inside a service host, which may have already started when tracing was enabled.</span></span>
4.  <span data-ttu-id="c4b5c-119">Starten Sie die auf WSDAPI basierende Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-119">Start the WSDAPI-based client application.</span></span> <span data-ttu-id="c4b5c-120">Die Anwendung, die gedebuggt wird, oder der WSD-Debugclient kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-120">The application being debugged or the WSD Debug Client can be used.</span></span>
5.  <span data-ttu-id="c4b5c-121">Reproduzieren Sie den Anwendungsfehler.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-121">Reproduce the application failure.</span></span>
6.  <span data-ttu-id="c4b5c-122">Beenden Sie die auf WSDAPI basierende Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-122">Terminate the WSDAPI-based client application.</span></span>
7.  <span data-ttu-id="c4b5c-123">Wenn der Prozess, der WinHTTP verwendet, nicht mit der Client Anwendung beendet wird, starten Sie den Computer neu.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-123">If the process using WinHTTP is not terminated with the client application, restart the computer.</span></span> <span data-ttu-id="c4b5c-124">Wenn z. b. die [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlungs-APIs verwendet werden, muss der Computer neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-124">For example, if the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) APIs are being used, the computer must be restarted.</span></span>
8.  <span data-ttu-id="c4b5c-125">Führen Sie den folgenden Befehl aus: **netsh WinHTTP Set Tracing State = deaktiviert** .</span><span class="sxs-lookup"><span data-stu-id="c4b5c-125">Run the following command: **netsh winhttp set tracing state=disabled**</span></span>

    <span data-ttu-id="c4b5c-126">Mit diesem Befehl wird die WinHTTP-Protokollierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-126">This command disables WinHTTP logging.</span></span>

9.  <span data-ttu-id="c4b5c-127">Überprüfen Sie die DPWS-Protokolle in C: \\ Temp, und überprüfen Sie, ob die erforderlichen Anforderungen und Nachrichten gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-127">Inspect the DPWS logs in C:\\Temp and verify that the required requests and messages were sent.</span></span>
10. <span data-ttu-id="c4b5c-128">Wenn die HTTPS-Kommunikation (Secure Channel) verwendet wird, überprüfen Sie auf SSL/TLS-Fehler.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-128">If secure channel (HTTPS) communication is being used, check for SSL/TLS failures.</span></span>

<span data-ttu-id="c4b5c-129">Nachdem WinHTTP-Protokolle erfasst wurden, können die Protokolle untersucht werden, um die Ursache für einen WSDAPI-Anwendungsfehler zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-129">Once WinHTTP logs have been captured, the logs can be examined to look for the cause of a WSDAPI application failure.</span></span> <span data-ttu-id="c4b5c-130">Beachten Sie, dass der Text-Editor, der zum Anzeigen dieser Protokolle verwendet wird, als Administrator ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="c4b5c-130">Note that the text editor used to view these logs must be run as Administrator.</span></span> <span data-ttu-id="c4b5c-131">Weitere Informationen finden Sie unter [Verwenden der WinHTTP-Protokollierung zum Überprüfen von Datenverkehr](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="c4b5c-131">For more information, see [Using WinHTTP Logging to Verify Get Traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4b5c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4b5c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4b5c-133">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c4b5c-133">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="c4b5c-134">Verwenden der WinHTTP-Protokollierung zum Überprüfen von Daten</span><span class="sxs-lookup"><span data-stu-id="c4b5c-134">Using WinHTTP Logging to Verify Get Traffic</span></span>](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
