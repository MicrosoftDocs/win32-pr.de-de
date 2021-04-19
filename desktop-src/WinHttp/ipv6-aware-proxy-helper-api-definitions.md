---
description: Um die von IPv6 aktivierten Funktionen nutzen zu können, müssen IT-Administratoren innerhalb Ihres WPAD-Skripts definieren, eine Funktion mit dem Namen "findproxyforurlex (URL, Host)", die die Legacy Funktion "FindProxyForURL (URL, Host)" ersetzt.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: API-Definitionen für IPv6-Aware Proxy-Hilfsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349631"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a><span data-ttu-id="e6a4b-103">API-Definitionen für IPv6-Aware Proxy-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="e6a4b-103">IPv6-Aware Proxy Helper API Definitions</span></span>

<span data-ttu-id="e6a4b-104">Um die von IPv6 aktivierten Funktionen nutzen zu können, müssen IT-Administratoren innerhalb Ihres WPAD-Skripts definieren, eine Funktion mit dem Namen "findproxyforurlex (URL, Host)", die die Legacy Funktion "FindProxyForURL (URL, Host)" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-104">In order to take advantage of the IPv6 enabled functions, IT administrators must define within their WPAD script, a function called FindProxyForURLEx (url, host) which will replace the legacy FindProxyForUrl (url, host) function.</span></span> <span data-ttu-id="e6a4b-105">Nur aus der neuen findproxyforurlex-Funktion können Administratoren die neuen Funktionen ausführen.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-105">Only from the new FindProxyForURLEx function will administrators be able to execute the new functions.</span></span>

<span data-ttu-id="e6a4b-106">Wir haben auch versucht, die Arbeit für Entwickler zu vereinfachen, indem wir unsere Funktionen so ausrichten, dass verschiedene Typen von IP-Adressen in derselben Reihenfolge wie andere Netzwerkkomponenten zurückgegeben werden, insbesondere IPv6-Adressen, gefolgt von IPv4-Adressen (d.h. Aktuelles Verhalten für die getaddrinfo (..)-Funktion von Winsock).</span><span class="sxs-lookup"><span data-stu-id="e6a4b-106">We also attempted to simplify work for developers, by aligning our functions to return different types of IP addresses in the same order of preference as other networking components, specifically IPv6 addresses followed by IPv4 addresses (i.e. current behavior for Winsock’s getaddrinfo(..) function).</span></span>

<span data-ttu-id="e6a4b-107">Die folgenden Funktionen sind Erweiterungen der [PAC-Datei Format Spezifikation (Navigator Proxy Auto-config)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) , um WPAD-Skripts das Verarbeiten von IPv6-fähigen Netzwerken zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-107">The following functions are extensions to the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) to enable WPAD scripts to handle IPv6 capable networks.</span></span>

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a><span data-ttu-id="e6a4b-108">Vordefinierte Funktionen und Umgebung für die JavaScript-Funktion findproxyforurlex</span><span class="sxs-lookup"><span data-stu-id="e6a4b-108">Predefined Functions and Environment for the JavaScript Function FindProxyforURLEx</span></span>

<span data-ttu-id="e6a4b-109">Hostname-basierte Bedingungen</span><span class="sxs-lookup"><span data-stu-id="e6a4b-109">Hostname based conditions</span></span>

<dl> <dt>

[<span data-ttu-id="e6a4b-110">**isresolvableex**</span><span class="sxs-lookup"><span data-stu-id="e6a4b-110">**isResolvableEx**</span></span>](isresolvableex.md)
</dt> <dd>

<span data-ttu-id="e6a4b-111">Bestimmt, ob eine angegebene Host Zeichenfolge in eine IP-Adresse aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-111">Determines if a given host string can resolve to an IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="e6a4b-112">**isinnettex**</span><span class="sxs-lookup"><span data-stu-id="e6a4b-112">**isInNetEx**</span></span>](isinnetex.md)
</dt> <dd>

<span data-ttu-id="e6a4b-113">Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-113">Determines if an IP address is in a specific subnet.</span></span>

</dd> </dl>

<span data-ttu-id="e6a4b-114">Zugehörige Utility-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e6a4b-114">Related utility functions</span></span>

<dl> <dt>

[<span data-ttu-id="e6a4b-115">**dnsresolveex**</span><span class="sxs-lookup"><span data-stu-id="e6a4b-115">**dnsResolveEx**</span></span>](dnsresolveex.md)
</dt> <dd>

<span data-ttu-id="e6a4b-116">Auflösen einer Host Zeichenfolge in die zugehörige IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-116">Resolve a host string to its IP address.</span></span>

</dd> <dt>

[<span data-ttu-id="e6a4b-117">**myIPAddressEx**</span><span class="sxs-lookup"><span data-stu-id="e6a4b-117">**myIPAddressEx**</span></span>](myipaddressex.md)
</dt> <dd>

<span data-ttu-id="e6a4b-118">Sucht alle IP-Adressen für localhost.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-118">Finds all the IP addresses for localhost.</span></span>

</dd> <dt>

[<span data-ttu-id="e6a4b-119">**"menpaddresslist"**</span><span class="sxs-lookup"><span data-stu-id="e6a4b-119">**sortIpAddressList**</span></span>](sortipaddresslist.md)
</dt> <dd>

<span data-ttu-id="e6a4b-120">Sortiert eine Liste von IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-120">Sorts a list of IP addresses.</span></span>

</dd> <dt>

[<span data-ttu-id="e6a4b-121">**GetClientVersion**</span><span class="sxs-lookup"><span data-stu-id="e6a4b-121">**getClientVersion**</span></span>](getclientversion.md)
</dt> <dd>

<span data-ttu-id="e6a4b-122">Ruft die Version der WPAD-Verarbeitungs-Engine ab.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-122">Gets the version of the WPAD processing engine.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="e6a4b-123">Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e6a4b-123">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



