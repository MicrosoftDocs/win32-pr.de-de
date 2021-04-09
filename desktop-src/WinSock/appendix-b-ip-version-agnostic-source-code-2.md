---
description: Dieser Anhang veranschaulicht eine umgeschriebene Version der simplec. c-und simples. c-Beispielanwendungen, die entweder IPv4-oder IPv6. IPv6-aktivierte Client CodeIPv6-Enabled Server Code ordnungsgemäß verarbeitet.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Anhang B: Quell Code für die unabhängige IP-Version'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862592"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a><span data-ttu-id="e12ae-103">Anhang B: Quell Code für die unabhängige IP-Version</span><span class="sxs-lookup"><span data-stu-id="e12ae-103">Appendix B: IP-version Agnostic Source Code</span></span>

<span data-ttu-id="e12ae-104">Dieser Anhang veranschaulicht eine umgeschriebene Version der simplec. c-und simples. c-Beispielanwendungen, die entweder IPv4 oder IPv6 ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e12ae-104">This appendix illustrates a rewritten version of the Simplec.c and Simples.c sample applications that gracefully handles either IPv4 or IPv6.</span></span>

-   [<span data-ttu-id="e12ae-105">IPv6-fähiger Client Code</span><span class="sxs-lookup"><span data-stu-id="e12ae-105">IPv6-Enabled Client Code</span></span>](ipv6-enabled-client-code-2.md)
-   [<span data-ttu-id="e12ae-106">IPv6-fähiger Server Code</span><span class="sxs-lookup"><span data-stu-id="e12ae-106">IPv6-Enabled Server Code</span></span>](ipv6-enabled-server-code-2.md)

<span data-ttu-id="e12ae-107">Dieser Code veranschaulicht die in diesem IPv6-Handbuch aufgeführten Richtlinien und ist enthalten, um Quellcode bereitzustellen, der erfolgreich geändert wurde, um Unterstützung für IPv6 hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e12ae-107">This code exemplifies the guidelines set forth in this IPv6 guide, and is included to provide source code that has been successfully modified to add support for IPv6.</span></span> <span data-ttu-id="e12ae-108">Dieses Beispiel ist absichtlich einfach, bietet aber ein praktisches Beispiel für die Verwendung und Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="e12ae-108">This sample is intentionally simple, but provides a hands-on sample for perusing and reviewing.</span></span> <span data-ttu-id="e12ae-109">Eine reine IPv4-Version dieses Quellcodes wird in [Anhang A: nur-IPv4-Quellcode](appendix-a-ipv4-only-source-code-2.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e12ae-109">An IPv4 only version of this source code is provided in [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md).</span></span>

<span data-ttu-id="e12ae-110">Wenn Sie den Quellcode in Anhang A (nur IPv4) und Anhang B (IP-Version agnostisch) vergleichen, erhalten Sie einen Eindruck von den Änderungen, die erforderlich sind, um die Windows Sockets-Anwendung so zu ändern, dass Unterstützung für IPv6 hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e12ae-110">By comparing the source code in Appendix A (IPv4 only) and Appendix B (IP-version agnostic), you get a sense of the changes necessary to modify your Windows Sockets application to add support for IPv6.</span></span>

 

 



