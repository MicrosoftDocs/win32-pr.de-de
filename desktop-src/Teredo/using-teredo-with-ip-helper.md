---
title: Verwenden von Teredo mit IP-Hilfsprogramm
description: Die IP-hilfsprogrammapi (Internet Protocol Helper) wird von einer Anwendung verwendet, um wichtige Informationen zur Netzwerkkonfiguration des lokalen Computers zu erfassen und bereitzustellen.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728480"
---
# <a name="using-teredo-with-ip-helper"></a><span data-ttu-id="f51d3-103">Verwenden von Teredo mit IP-Hilfsprogramm</span><span class="sxs-lookup"><span data-stu-id="f51d3-103">Using Teredo with IP Helper</span></span>

<span data-ttu-id="f51d3-104">Die IP Helper-API ( [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) ) wird von einer Anwendung verwendet, um wichtige Informationen zur Netzwerkkonfiguration des lokalen Computers zu sammeln und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f51d3-104">The [Internet Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (IP Helper) API is utilized by an application to gather and provide important information regarding the networking configuration of the local machine.</span></span> <span data-ttu-id="f51d3-105">Wenn Sie auf der Windows Vista-Plattform arbeiten, beinhalten diese Informationen den dynamischen UDP-Port, der der Teredo-Schnittstelle zugewiesen ist, sowie Änderungen, die möglicherweise am vorgesehenen Port vorgenommen werden</span><span class="sxs-lookup"><span data-stu-id="f51d3-105">When operating on the Windows Vista platform, this information includes the dynamic UDP port assigned to the Teredo interface and changes that may occur to the designated port.</span></span>

<span data-ttu-id="f51d3-106">Die folgenden Funktionen werden von der IP Helper-API verwendet, um die Verwendung der Teredo-Schnittstelle zu vereinfachen:</span><span class="sxs-lookup"><span data-stu-id="f51d3-106">The following functions are utilized by the IP Helper API to facilitate the use of the Teredo interface:</span></span>

-   [<span data-ttu-id="f51d3-107">**Getteredoport**</span><span class="sxs-lookup"><span data-stu-id="f51d3-107">**GetTeredoPort**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [<span data-ttu-id="f51d3-108">**Notifyteredoportchange**</span><span class="sxs-lookup"><span data-stu-id="f51d3-108">**NotifyTeredoPortChange**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [<span data-ttu-id="f51d3-109">**Notifystableunicastipadresssstable**</span><span class="sxs-lookup"><span data-stu-id="f51d3-109">**NotifyStableUnicastIpAddressTable**</span></span>](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 