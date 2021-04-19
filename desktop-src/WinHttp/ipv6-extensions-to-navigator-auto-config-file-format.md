---
description: Microsoft hat ein Array von Erweiterungen für das Auto-config-Datei Format des Navigators implementiert, um die IPv6-Unterstützung in WinInet-und WinHTTP WPAD-Hilfsfunktionen hinzuzufügen.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373267"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a><span data-ttu-id="59b26-103">IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators</span><span class="sxs-lookup"><span data-stu-id="59b26-103">IPv6 Extensions to Navigator Auto-Config File Format</span></span>

<span data-ttu-id="59b26-104">Microsoft hat ein Array von Erweiterungen für das Auto-config-Datei Format des Navigators implementiert, um die IPv6-Unterstützung in WinInet-und WinHTTP WPAD-Hilfsfunktionen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="59b26-104">Microsoft has implemented an array of extensions to the Navigator Auto-Config File Format in order to add IPv6 support in the WinINet and WinHTTP WPAD helper functions.</span></span>

<span data-ttu-id="59b26-105">Die Explosion des Internets in den späten 90er Jahren hat einen unerwarteten Mangel an IPv4-Adressen verursacht, wobei der Pool täglich erschöpft ist.</span><span class="sxs-lookup"><span data-stu-id="59b26-105">The explosion of the Internet in the late 1990’s has caused an unexpected scarcity of IPv4 addresses, with the pool depleting on a daily basis.</span></span> <span data-ttu-id="59b26-106">IPv6 bietet eine Lösung für dieses Problem, und obwohl es zurzeit nicht weit bereitgestellt ist, wird seine Verwendung in Zukunft definitiv stärker verbreitet.</span><span class="sxs-lookup"><span data-stu-id="59b26-106">IPv6 provides a solution to this problem and although it is currently not widely deployed, its use will definitely become more prevalent in the future.</span></span> <span data-ttu-id="59b26-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) ist ein Protokoll, mit dem Webclients automatisch erkennen können, welche Proxykonfiguration für den ausgehenden Datenverkehr vorgesehen sein sollte.</span><span class="sxs-lookup"><span data-stu-id="59b26-107">[WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) is a protocol that allows web clients to automatically detect what the correct proxy configuration should be for their outgoing traffic.</span></span> <span data-ttu-id="59b26-108">Dies ist für Unternehmens Bereitstellungen sehr nützlich, da IT-Administratoren komplexe Skripts einrichten können, die den Datenverkehr für alle Clients basierend auf dem Zielserver, mit dem die Clients eine Verbindung herstellen möchten, an bestimmte Proxys weiterleiten können.</span><span class="sxs-lookup"><span data-stu-id="59b26-108">This is very useful for corporate deployments because it allows IT administrators to setup complex scripts that can route traffic for all clients to specific proxies based on the target server the clients are attempting to connect to.</span></span> <span data-ttu-id="59b26-109">WinInet und WinHTTP unterstützen WPAD-Hilfsobjekte entsprechend der Definition der [PAC-Datei Format Spezifikation (Navigator Proxy Auto-config)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), die zu einem Standardwert geworden ist.</span><span class="sxs-lookup"><span data-stu-id="59b26-109">WinINet and WinHTTP support WPAD helper functions as defined by the [Navigator Proxy Auto-Config (PAC) File Format specification](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), which has become a defacto standard.</span></span> <span data-ttu-id="59b26-110">Leider wurde diese Spezifikation in 1996 geschrieben und definiert nicht, was das Verhalten der Funktion sein sollte, wenn ein WPAD-Skript in einem IPv6-fähigen Netzwerk bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="59b26-110">Unfortunately this specification was written in 1996 and does not define what the function behaviors should be when a WPAD script is deployed in an IPv6 capable network.</span></span>

<span data-ttu-id="59b26-111">Da IPv6 die Welle der Zukunft ist, unterstützen alle Windows-Komponenten jetzt Dual Stack-(IPv4-und IPv6-) und reine IPv6-Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="59b26-111">Since IPv6 is the wave of the future, all Windows components now support dual stack (IPv4 and IPv6) and IPv6 only networks.</span></span> <span data-ttu-id="59b26-112">Um IPv6 zu unterstützen, ohne die vorhandene Bereitstellung zu beeinträchtigen, hat Microsoft sechs neue Hilfsklassen Funktionen als Erweiterung der PAC-Datei Format Spezifikation (Navigator Proxy Auto-config) hinzugefügt und außerdem eine neue IPv6-fähige Funktion namens " **findproxyforurlex** " hinzugefügt, die Administratoren im WPAD-Skript implementieren können.</span><span class="sxs-lookup"><span data-stu-id="59b26-112">In order to support IPv6 without affecting existing deployment, Microsoft added 6 new helper class functions as an extension to the Navigator Proxy Auto-Config (PAC) File Format specification and also added a new IPv6 capable function called **FindProxyForURLEx** that administrators can implement in the WPAD script.</span></span>

<dl> <dt>

[<span data-ttu-id="59b26-113">IPv6-abhängige proxyhilfsobjekts-Definitionen</span><span class="sxs-lookup"><span data-stu-id="59b26-113">IPv6-Aware Proxy Helper API Definitions</span></span>](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[<span data-ttu-id="59b26-114">Unterschiede zwischen IPv6-Aware WPAD-Hilfsfunktionen und älteren WPAD-Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="59b26-114">Differences Between IPv6-Aware WPAD Helper Functions and Legacy WPAD Helper Functions</span></span>](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
<span data-ttu-id="59b26-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="59b26-115"></dt> <dd></dd> </dl></span></span>

> [!Note]  
> <span data-ttu-id="59b26-116">Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="59b26-116">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



