---
description: Die Langlebigkeit von IPv4 führte dazu, dass viele bekannte IPv4-Adressen hart codiert werden, wie z. b. Loopback Adressen (127. x. x. x), ganzzahlige Konstanten wie z. b. inaddr \_ Loopback.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Verwendung von hart codierten IPv4-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343458"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a><span data-ttu-id="153c1-103">Verwendung von hart codierten IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="153c1-103">Use of Hardcoded IPv4 Addresses</span></span>

<span data-ttu-id="153c1-104">Die Langlebigkeit von IPv4 führte dazu, dass viele bekannte IPv4-Adressen hart codiert werden, wie z. b. Loopback Adressen (127. x. x. x), ganzzahlige Konstanten wie z. b. inaddr \_ Loopback.</span><span class="sxs-lookup"><span data-stu-id="153c1-104">The longevity of IPv4 resulted in hard coding many well-known IPv4 addresses, such as loopback addresses (127.x.x.x), integer constants such as INADDR\_LOOPBACK, among others.</span></span> <span data-ttu-id="153c1-105">Die Praxis der hart Codierung dieser Adressen stellt offensichtliche Probleme dar, wenn und vorhandene Anwendungen geändert werden, um IPv6 zu unterstützen oder neue, von der Version unabhängige Programme zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="153c1-105">The practice of hard coding these addresses presents obvious problems when modifying and existing application to support IPv6 or creating new IP version-independent programs.</span></span>

<span data-ttu-id="153c1-106">Bewährte Methode</span><span class="sxs-lookup"><span data-stu-id="153c1-106">Best Practice</span></span>

-   <span data-ttu-id="153c1-107">Der beste Ansatz besteht darin, die hart Codierung von Adressen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="153c1-107">The best approach is to avoid hardcoding any addresses.</span></span>

<span data-ttu-id="153c1-108">Zu Vermeider Code</span><span class="sxs-lookup"><span data-stu-id="153c1-108">Code To Avoid</span></span>

-   <span data-ttu-id="153c1-109">Vermeiden Sie die Verwendung von hart codierten Adressen im Code.</span><span class="sxs-lookup"><span data-stu-id="153c1-109">Avoid using hardcoded addresses in code.</span></span>

<span data-ttu-id="153c1-110">**So ändern Sie die vorhandene Codebasis von IPv4 zu IPv4-und IPv6-Interoperabilität**</span><span class="sxs-lookup"><span data-stu-id="153c1-110">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="153c1-111">Erwerben Sie das *Checkv4.exe* -Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="153c1-111">Acquire the *Checkv4.exe* utility.</span></span> <span data-ttu-id="153c1-112">Das *Checkv4.exe* -Hilfsprogramm wird als Teil des Microsoft Windows Software Development Kit (SDK) installiert, das für Windows Vista und höher veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="153c1-112">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later.</span></span> <span data-ttu-id="153c1-113">Der Windows SDK ist über ein MSDN-Abonnement verfügbar und kann auch von der Microsoft-Website heruntergeladen werden ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="153c1-113">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span>
2.  <span data-ttu-id="153c1-114">Führen Sie das *Checkv4.exe* -Hilfsprogramm für den Code aus.</span><span class="sxs-lookup"><span data-stu-id="153c1-114">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="153c1-115">Erfahren Sie, wie Sie das *Checkv4.exe* -Hilfsprogramm für Ihre Dateien ausführen, [indem Sie das Checkv4.exe-Hilfsprogramm verwenden](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="153c1-115">Learn about how to run the *Checkv4.exe* utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="153c1-116">Das *Checkv4.exe* -Hilfsprogramm warnt Sie bei der Anwesenheit allgemeiner Definitionen für IPv4-Adressen, z. b. inaddr- \_ Loopback.</span><span class="sxs-lookup"><span data-stu-id="153c1-116">The *Checkv4.exe* utility alerts you to the presence of common defines for IPv4 addresses, such as INADDR\_LOOPBACK.</span></span> <span data-ttu-id="153c1-117">Ändern Sie den Code, der Literalzeichenfolgen verwendet, mit Code, der Protokoll Versions agnostisch ist.</span><span class="sxs-lookup"><span data-stu-id="153c1-117">Modify any code that uses literal strings with code that is protocol-version agnostic.</span></span>
4.  <span data-ttu-id="153c1-118">Durchsuchen Sie die Codebasis nach anderen möglichen Literalzeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="153c1-118">Search your code base for other potential literal strings, as appropriate.</span></span>

<span data-ttu-id="153c1-119">Mit dem *Checkv4.exe* -Hilfsprogramm können Sie allgemeine Literalzeichenfolgen finden, aber es gibt möglicherweise andere, die für Ihre Anwendung spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="153c1-119">The *Checkv4.exe* utility can help you find common literal strings, but there may be others that are specific to your application.</span></span> <span data-ttu-id="153c1-120">Sie sollten eine gründliche Suche und Tests durchführen, um sicherzustellen, dass die Codebasis mögliche Probleme mit Literalzeichenfolgen beseitigt hat.</span><span class="sxs-lookup"><span data-stu-id="153c1-120">You should perform thorough searching and testing to ensure your code base has eradicated potential problems associated with literal strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="153c1-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="153c1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="153c1-122">IPv6-Handbuch für Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="153c1-122">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="153c1-123">Ändern von Datenstrukturen für IPv6-Winsock-Appications</span><span class="sxs-lookup"><span data-stu-id="153c1-123">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="153c1-124">Dual-Stack-Sockets für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="153c1-124">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="153c1-125">Funktionsaufrufe für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="153c1-125">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="153c1-126">Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="153c1-126">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="153c1-127">Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="153c1-127">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 



