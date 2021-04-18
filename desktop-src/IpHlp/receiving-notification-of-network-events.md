---
description: Verwenden Sie die folgenden Funktionen, um sicherzustellen, dass eine Anwendung Benachrichtigungen über bestimmte Netzwerkereignisse empfängt.
ms.assetid: e1ca5abf-83c2-44f0-8049-ddf1b81ef088
title: Empfangen von Benachrichtigungen über Netzwerkereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb9840f7ddf4adbfaae5775de337da81a3e7670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345085"
---
# <a name="receiving-notification-of-network-events"></a><span data-ttu-id="616fd-103">Empfangen von Benachrichtigungen über Netzwerkereignisse</span><span class="sxs-lookup"><span data-stu-id="616fd-103">Receiving Notification of Network Events</span></span>

<span data-ttu-id="616fd-104">Verwenden Sie die folgenden Funktionen, um sicherzustellen, dass eine Anwendung Benachrichtigungen über bestimmte Netzwerkereignisse empfängt.</span><span class="sxs-lookup"><span data-stu-id="616fd-104">Use the following functions to ensure that an application receives notification of certain network events.</span></span>

<span data-ttu-id="616fd-105">Verwenden Sie die [**notifyaddrchange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) -Funktion, um eine Benachrichtigung über jede Änderung anzufordern, die bei der Zuordnung zwischen IP-Adressen und Schnittstellen auf dem lokalen Computer auftritt.</span><span class="sxs-lookup"><span data-stu-id="616fd-105">Use the [**NotifyAddrChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyaddrchange) function to request notification of any change that occurs in the mapping between IP addresses and interfaces on the local computer.</span></span>

<span data-ttu-id="616fd-106">Ebenso ermöglicht die [**notifyroutechange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) -Funktion einer Anwendung, eine Benachrichtigung über jede Änderung anzufordern, die in der IP-Routing Tabelle auftritt.</span><span class="sxs-lookup"><span data-stu-id="616fd-106">Similarly, the [**NotifyRouteChange**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-notifyroutechange) function enables an application to request notification of any change that occurs in the IP routing table.</span></span>

<span data-ttu-id="616fd-107">Die von diesen Funktionen bereitgestellten Benachrichtigungen geben nicht an, was geändert wurde. Sie geben einfach an, dass sich etwas geändert hat.</span><span class="sxs-lookup"><span data-stu-id="616fd-107">The notifications provided by these functions do not specify what changed; they simply specify that something changed.</span></span> <span data-ttu-id="616fd-108">Verwenden Sie andere IP-Hilfsfunktionen, wie z. b. [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) und [**getbestroute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), um die genaue Natur der Änderung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="616fd-108">Use other IP Helper functions, such as [**GetIPAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) and [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute), to determine the exact nature of the change.</span></span>

 

 



