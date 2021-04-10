---
description: Dieses Handbuch enthält die Informationen, die Sie benötigen, um Ihre Microsoft Windows-Anwendung für die Verwendung der nächsten Generation von Internet Protocol, Version 6 (IPv6), zu aktivieren.
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: IPv6-Handbuch für Windows Sockets-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129169"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a><span data-ttu-id="c295d-103">IPv6-Handbuch für Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c295d-103">IPv6 Guide for Windows Sockets Applications</span></span>

<span data-ttu-id="c295d-104">Dieses Handbuch enthält die Informationen, die Sie benötigen, um Ihre Microsoft Windows-Anwendung für die Verwendung der nächsten Generation von Internet Protocol, Version 6 (IPv6), zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c295d-104">This guide provides the information you need to enable your Microsoft Windows application to use the next generation of Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="c295d-105">Das Hinzufügen von IPv6-Funktionen zu Ihrer Anwendung ist nicht notwendigerweise ein Portierungs Prozess.</span><span class="sxs-lookup"><span data-stu-id="c295d-105">Adding IPv6 capability to your application is not necessarily a porting process.</span></span> <span data-ttu-id="c295d-106">Um eine Anwendung zu portieren, empfiehlt es sich, Code so zu ändern, dass er auf einer anderen Plattform funktioniert</span><span class="sxs-lookup"><span data-stu-id="c295d-106">To port an application suggests modifying code to work on a different platform, which implies leaving the previous platform behind.</span></span> <span data-ttu-id="c295d-107">Dieses Handbuch ist speziell so strukturiert, dass einer Anwendung IPv6-Funktionen hinzugefügt werden können, während IPv4-Funktionen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="c295d-107">This guide is specifically structured to help add IPv6 capability to an application while retaining IPv4 functionality.</span></span>

<span data-ttu-id="c295d-108">In diesem Leitfaden werden die Probleme im Zusammenhang mit dem Hinzufügen von IPv6-Funktionen erläutert. Anschließend werden die Entwicklungsbereiche als Ziel des Übergangs behandelt.</span><span class="sxs-lookup"><span data-stu-id="c295d-108">This guide discusses the issues associated with adding IPv6 functionality, then targets the areas of development most affected by the transition.</span></span> <span data-ttu-id="c295d-109">Jeder Bereich erhält eine ausführliche Erläuterung der zu überwachenden Fehler, der Strategien, die zur Vermeidung von Problemen vorgeschlagen werden, und Tipps, wie Sie neue programmgesteuerte Elemente von [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (Funktionen und Strukturen) optimal nutzen können.</span><span class="sxs-lookup"><span data-stu-id="c295d-109">Each area receives a thorough explanation of the pitfalls to watch out for, the strategies suggested to avoid them, and tips on how to make the best use of new [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) programmatic elements (functions and structures).</span></span> <span data-ttu-id="c295d-110">Weitere Informationen zu IPv6 finden Sie [unter IPv6-Unterstützung](ipv6-support-2.md).</span><span class="sxs-lookup"><span data-stu-id="c295d-110">For additional information on IPv6, see [IPv6 Support](ipv6-support-2.md).</span></span>

<span data-ttu-id="c295d-111">Dieses Handbuch enthält auch Codebeispiele, mit denen Sie praktische Erfahrungen und visuelle Darstellungen der Probleme erhalten können, die beim Ändern Ihrer Anwendungen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="c295d-111">This guide also provides code examples to give you hands-on experience and visual representations of the issues you could encounter when modifying your applications.</span></span> <span data-ttu-id="c295d-112">Die Beispiele stammen aus den umfassenden, funktionierenden Beispielen einer einfachen Windows Sockets-Anwendung, die zur Unterstützung von IPv4 und IPv6 geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c295d-112">The examples come from complete, working examples of a simple Windows Sockets application that has been modified to support both IPv4 and IPv6.</span></span> <span data-ttu-id="c295d-113">Der Quellcode für diese funktionierenden Beispiele ist vollständig in zwei Anhänge am Ende dieses Dokuments enthalten: [Anhang A: nur-IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md) enthält den Quellcode für eine Anwendung, bevor Sie zur Unterstützung von IPv6 geändert wird. [Anhang B:](appendix-b-ip-version-agnostic-source-code-2.md) der Quellcode für die unabhängige IP-Version stellt den Quellcode bereit, nachdem die Anwendung IPv6-aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="c295d-113">Source code for these working examples is included in its entirety in two appendixes at the end of this document: [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) includes the source code for an application before it is modified to support IPv6; [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md) provides the source code after the application has been IPv6-enabled.</span></span>

<span data-ttu-id="c295d-114">Microsoft stellt ein Dienstprogramm namens Checkv4.exe bereit, mit dessen Hilfe Sie potenziell Portierungs relevanten Code in Ihrem Anwendungscode finden und auch Empfehlungen für Korrekturen erhalten.</span><span class="sxs-lookup"><span data-stu-id="c295d-114">Microsoft provides a utility called Checkv4.exe that helps you find potentially porting-sensitive code in your application code, and also makes recommendations for fixes.</span></span> <span data-ttu-id="c295d-115">Das Checkv4.exe-Hilfsprogramm wird in diesem Dokument mit der Beispielanwendung, die in den Appendixes enthalten ist, zusammen mit Bildschirmfotos veranschaulicht, die die Ausgabe des Checkv4.exe Hilfsprogramms anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c295d-115">The Checkv4.exe utility is demonstrated in this document, using the sample application included in the appendixes, along with screen shots displaying the output that the Checkv4.exe utility produces.</span></span> <span data-ttu-id="c295d-116">Weitere Informationen finden Sie unter [Verwenden des Checkv4.exe Hilfsprogramms](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="c295d-116">For more information, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>

<span data-ttu-id="c295d-117">Die in diesem Handbuch behandelten Programmier Bereiche lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c295d-117">The programming areas addressed by this guide are:</span></span>

-   [<span data-ttu-id="c295d-118">Ändern von Datenstrukturen für IPv6-Winsock-Appications</span><span class="sxs-lookup"><span data-stu-id="c295d-118">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
-   [<span data-ttu-id="c295d-119">Funktionsaufrufe für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c295d-119">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
-   [<span data-ttu-id="c295d-120">Verwendung von hart codierten IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="c295d-120">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
-   [<span data-ttu-id="c295d-121">Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c295d-121">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
-   [<span data-ttu-id="c295d-122">Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c295d-122">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
-   [<span data-ttu-id="c295d-123">Dual-Stack-Sockets für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="c295d-123">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)

<span data-ttu-id="c295d-124">Da es keine einheitliche Abfolge von Ereignissen gibt, werden die Abschnitte, die Probleme mit der IPv6-Aktivierung behandeln, nicht nacheinander angeordnet, sodass Sie jederzeit auf jeden Abschnitt verweisen können.</span><span class="sxs-lookup"><span data-stu-id="c295d-124">Because there is no uniform sequence of events, the sections that address IPv6-enabling issues are not arranged in a sequentially significant manner, so you can reference any section at any time.</span></span> <span data-ttu-id="c295d-125">Es wird dringend empfohlen, jeden Abschnitt zu überprüfen, während Sie der Anwendung IPv6-Funktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c295d-125">It is strongly recommended that you review each section while adding IPv6 capability to your application.</span></span> <span data-ttu-id="c295d-126">Außerdem empfiehlt es sich, über das Checkv4.exe-Hilfsprogramm zu lesen, da es Tipps zur Reihenfolge enthält, in der Probleme mit der IPv6-Aktivierung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="c295d-126">It is also advisable to read about the Checkv4.exe utility, as it includes tips on the order in which to address IPv6-enabling issues.</span></span>

<span data-ttu-id="c295d-127">Weitere Informationen zum Checkv4.exe-Hilfsprogramm und zum Überprüfen der Reihenfolge, in der Sie den Portierungs Prozess in Ihren Anwendungen verwenden sollten, finden Sie unter [Verwenden des Checkv4.exe Hilfsprogramms](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="c295d-127">To look at the Checkv4.exe utility, and to review the order in which you should approach the porting process in your applications, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span> <span data-ttu-id="c295d-128">Dieser Abschnitt enthält Informationen zu einem Kompilierzeit Kennzeichen, das strikt auf Programmierungs Elemente überprüft, die mit IPv6 nicht kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="c295d-128">This section includes information on a compile-time flag that strictly checks for programming elements incompatible with IPv6.</span></span>

<span data-ttu-id="c295d-129">Um direkt zur Beispielanwendung zu wechseln, finden Sie weitere Informationen unter [Anhang A: nur-IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md) und [Anhang B: Quell Code, der der IP-Version agnostisch](appendix-b-ip-version-agnostic-source-code-2.md)ist.</span><span class="sxs-lookup"><span data-stu-id="c295d-129">To go straight to the sample application, see [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) and [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c295d-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c295d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c295d-131">Internet Protokoll Version 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="c295d-131">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="c295d-132">IPv6-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="c295d-132">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="c295d-133">IPv6-Technologievorschau für Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c295d-133">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[<span data-ttu-id="c295d-134">Verwenden des Checkv4.exe Hilfsprogramms</span><span class="sxs-lookup"><span data-stu-id="c295d-134">Using the Checkv4.exe Utility</span></span>](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[<span data-ttu-id="c295d-135">Anhang A: nur-IPv4-Quellcode</span><span class="sxs-lookup"><span data-stu-id="c295d-135">Appendix A: IPv4-only Source Code</span></span>](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[<span data-ttu-id="c295d-136">Anhang B: Quell Code für die unabhängige IP-Version</span><span class="sxs-lookup"><span data-stu-id="c295d-136">Appendix B: IP-version Agnostic Source Code</span></span>](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



