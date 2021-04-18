---
title: Remotedesktopprotokoll
description: Das Microsoft-Remotedesktop Protokoll (RDP) bietet Remote Anzeige-und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Remotedesktopprotokoll (RDP) Remotedesktopdienste
- RDP (siehe Remotedesktopprotokoll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338467"
---
# <a name="remote-desktop-protocol"></a><span data-ttu-id="c619d-105">Remotedesktopprotokoll</span><span class="sxs-lookup"><span data-stu-id="c619d-105">Remote Desktop Protocol</span></span>

<span data-ttu-id="c619d-106">Das Microsoft-Remotedesktop Protokoll (RDP) bietet Remote Anzeige-und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c619d-106">The Microsoft Remote Desktop Protocol (RDP) provides remote display and input capabilities over network connections for Windows-based applications running on a server.</span></span> <span data-ttu-id="c619d-107">RDP wurde entwickelt, um unterschiedliche Arten von Netzwerktopologien und mehreren LAN-Protokollen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c619d-107">RDP is designed to support different types of network topologies and multiple LAN protocols.</span></span>

> [!Note]  
> <span data-ttu-id="c619d-108">Dieses Thema ist für Softwareentwickler konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c619d-108">This topic is for software developers.</span></span> <span data-ttu-id="c619d-109">Wenn Sie nach Benutzerinformationen für Remotedesktop suchen, finden Sie weitere Informationen [unter Windows-Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span><span class="sxs-lookup"><span data-stu-id="c619d-109">If you are looking for user information for Remote Desktop, see [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8).</span></span> <span data-ttu-id="c619d-110">Informationen zu Remotedesktop finden Sie unter [Remotedesktopdienste auf TechNet](/windows/deployment/deploy-whats-new).</span><span class="sxs-lookup"><span data-stu-id="c619d-110">If you are looking for IT professional information for Remote Desktop, see [Remote Desktop Services on TechNet](/windows/deployment/deploy-whats-new).</span></span>

 

## <a name="basic-architecture"></a><span data-ttu-id="c619d-111">Grundlegende Architektur</span><span class="sxs-lookup"><span data-stu-id="c619d-111">Basic Architecture</span></span>

<span data-ttu-id="c619d-112">RDP basiert auf und einer Erweiterung von, der ITU T. 120-Familie von Protokollen.</span><span class="sxs-lookup"><span data-stu-id="c619d-112">RDP is based on, and an extension of, the ITU T.120 family of protocols.</span></span> <span data-ttu-id="c619d-113">RDP ist ein Verwaltungs Protokoll mit mehreren Kanälen, das getrennte virtuelle Kanäle für das Ausführen von Gerätekommunikation und Präsentationsdaten vom Server sowie verschlüsselte clientmaus-und Tastatur Daten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c619d-113">RDP is a multiple-channel capable protocol that allows for separate virtual channels for carrying device communication and presentation data from the server, as well as encrypted client mouse and keyboard data.</span></span> <span data-ttu-id="c619d-114">RDP stellt eine erweiterbare Basis bereit und unterstützt bis zu 64.000 separate Kanäle für die Datenübertragung und die Bereitstellung von Multipoint-Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="c619d-114">RDP provides an extensible base and supports up to 64,000 separate channels for data transmission and provisions for multipoint transmission.</span></span>

<span data-ttu-id="c619d-115">Auf dem Server verwendet RDP seinen eigenen Videotreiber zum Rendern der Anzeige Ausgabe, indem die Renderinginformationen mithilfe des RDP-Protokolls in Netzwerkpakete erstellt und über das Netzwerk an den Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c619d-115">On the server, RDP uses its own video driver to render display output by constructing the rendering information into network packets by using RDP protocol and sending them over the network to the client.</span></span> <span data-ttu-id="c619d-116">Auf dem Client empfängt RDP Renderingdaten und interpretiert die Pakete in entsprechende API-Aufrufe von Microsoft Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="c619d-116">On the client, RDP receives rendering data and interprets the packets into corresponding Microsoft Windows graphics device interface (GDI) API calls.</span></span> <span data-ttu-id="c619d-117">Für den Eingabe Pfad werden Client Maus-und Tastatur Ereignisse vom Client an den Server umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c619d-117">For the input path, client mouse and keyboard events are redirected from the client to the server.</span></span> <span data-ttu-id="c619d-118">Auf dem Server verwendet RDP seinen eigenen Tastatur-und Maustreiber, um diese Tastatur-und Mausereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c619d-118">On the server, RDP uses its own keyboard and mouse driver to receive these keyboard and mouse events.</span></span>

<span data-ttu-id="c619d-119">In einer Remotedesktop Sitzung werden alle Umgebungsvariablen – z. b. Variablen, die die Farb Tiefe und das Aktivieren und Deaktivieren von – festlegen, durch die RCP-Tcp Verbindungseinstellungen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c619d-119">In a Remote Desktop session, all environment variables—for example, variables determining color depth and wallpaper enabling and disabling—are determined by the RCP-Tcp connection settings.</span></span> <span data-ttu-id="c619d-120">Dies gilt für alle Funktionen und Methoden, die Umgebungsvariablen in der [Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md) und der [Remotedesktopdienste WMI-Anbieter Schnittstelle](terminal-services-wmi-provider-reference.md)festlegen.</span><span class="sxs-lookup"><span data-stu-id="c619d-120">This applies to all functions and methods that set environment variables in the [Remote Desktop Web Connection Reference](remote-desktop-web-connection-reference.md) and the [Remote Desktop Services WMI Provider interface](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="features"></a><span data-ttu-id="c619d-121">Features</span><span class="sxs-lookup"><span data-stu-id="c619d-121">Features</span></span>

<span data-ttu-id="c619d-122">Microsoft RDP umfasst die folgenden Features und Funktionen:</span><span class="sxs-lookup"><span data-stu-id="c619d-122">Microsoft RDP includes the following features and capabilities:</span></span>

<dl> <dt>

<span data-ttu-id="c619d-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Verschlüsselungs</span><span class="sxs-lookup"><span data-stu-id="c619d-123"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Encryption</span></span>
</dt> <dd>

<span data-ttu-id="c619d-124">RDP verwendet die RC4-Verschlüsselung der RSA-Sicherheit, eine streamchiffre, die zum effizienten Verschlüsseln kleiner Datenmengen konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="c619d-124">RDP uses RSA Security's RC4 cipher, a stream cipher designed to efficiently encrypt small amounts of data.</span></span> <span data-ttu-id="c619d-125">RC4 ist für die sichere Kommunikation über Netzwerke konzipiert.</span><span class="sxs-lookup"><span data-stu-id="c619d-125">RC4 is designed for secure communications over networks.</span></span> <span data-ttu-id="c619d-126">Administratoren können die Verschlüsselung von Daten mithilfe eines 56-oder 128-Bit-Schlüssels auswählen.</span><span class="sxs-lookup"><span data-stu-id="c619d-126">Administrators can choose to encrypt data by using a 56- or 128-bit key.</span></span>

</dd> <dt>

<span data-ttu-id="c619d-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Features zur Bandbreiten Reduzierung</span><span class="sxs-lookup"><span data-stu-id="c619d-127"><span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Bandwidth reduction features</span></span>
</dt> <dd>

<span data-ttu-id="c619d-128">RDP unterstützt verschiedene Mechanismen, um die Datenmenge zu reduzieren, die über eine Netzwerkverbindung übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="c619d-128">RDP supports various mechanisms to reduce the amount of data transmitted over a network connection.</span></span> <span data-ttu-id="c619d-129">Zu den Mechanismen zählen die Datenkomprimierung, das persistente Zwischenspeichern von Bitmaps und das Zwischenspeichern von Symbolen und Fragmenten im RAM.</span><span class="sxs-lookup"><span data-stu-id="c619d-129">Mechanisms include data compression, persistent caching of bitmaps, and caching of glyphs and fragments in RAM.</span></span> <span data-ttu-id="c619d-130">Der persistente Bitmap-Cache kann eine deutliche Verbesserung der Leistung gegenüber Verbindungen mit geringer Bandbreite bieten, insbesondere bei der Ausführung von Anwendungen, die große Bitmaps umfassend nutzen.</span><span class="sxs-lookup"><span data-stu-id="c619d-130">The persistent bitmap cache can provide a substantial improvement in performance over low-bandwidth connections, especially when running applications that make extensive use of large bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="c619d-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming getrennt</span><span class="sxs-lookup"><span data-stu-id="c619d-131"><span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming disconnect</span></span>
</dt> <dd>

<span data-ttu-id="c619d-132">Ein Benutzer kann die Verbindung mit einer Remote Desktop Sitzung manuell trennen, ohne sich abzumelden.</span><span class="sxs-lookup"><span data-stu-id="c619d-132">A user can manually disconnect from a remote desktop session without logging off.</span></span> <span data-ttu-id="c619d-133">Der Benutzer wird automatisch erneut mit der getrennten Sitzung verbunden, wenn er sich wieder beim System anmeldet, entweder vom gleichen Gerät oder von einem anderen Gerät aus.</span><span class="sxs-lookup"><span data-stu-id="c619d-133">The user is automatically reconnected to their disconnected session when he or she logs back onto the system, either from the same device or a different device.</span></span> <span data-ttu-id="c619d-134">Wenn die Sitzung eines Benutzers unerwartet durch einen Netzwerk-oder Client Fehler beendet wird, wird der Benutzer getrennt, aber nicht abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="c619d-134">When a user's session is unexpectedly terminated by a network or client failure, the user is disconnected but not logged off.</span></span>

</dd> <dt>

<span data-ttu-id="c619d-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Zwischenablage Zuordnung</span><span class="sxs-lookup"><span data-stu-id="c619d-135"><span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Clipboard mapping</span></span>
</dt> <dd>

<span data-ttu-id="c619d-136">Benutzer können Text und Grafiken zwischen Anwendungen, die auf dem lokalen Computer ausgeführt werden, und die, die in einer Remote Desktop Sitzung ausgeführt werden, sowie zwischen Sitzungen löschen, kopieren und einfügen.</span><span class="sxs-lookup"><span data-stu-id="c619d-136">Users can delete, copy, and paste text and graphics between applications running on the local computer and those running in a remote desktop session, and between sessions.</span></span>

</dd> <dt>

<span data-ttu-id="c619d-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Druck Umleitung</span><span class="sxs-lookup"><span data-stu-id="c619d-137"><span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Print redirection</span></span>
</dt> <dd>

<span data-ttu-id="c619d-138">Anwendungen, die in einer Remote Desktop Sitzung ausgeführt werden, können auf einen Drucker drucken, der an das Client Gerät angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c619d-138">Applications running within a remote desktop session can print to a printer attached to the client device.</span></span>

</dd> <dt>

<span data-ttu-id="c619d-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtuelle Kanäle</span><span class="sxs-lookup"><span data-stu-id="c619d-139"><span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtual channels</span></span>
</dt> <dd>

<span data-ttu-id="c619d-140">Mithilfe der virtuellen RDP-Kanal Architektur können vorhandene Anwendungen erweitert werden, und neue Anwendungen können entwickelt werden, um Funktionen hinzuzufügen, für die eine Kommunikation zwischen dem Client Gerät und einer Anwendung erforderlich ist, die in einer Remote Desktop Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c619d-140">By using RDP virtual channel architecture, existing applications can be augmented and new applications can be developed to add features that require communications between the client device and an application running in a remote desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="c619d-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote Steuerung</span><span class="sxs-lookup"><span data-stu-id="c619d-141"><span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote control</span></span>
</dt> <dd>

<span data-ttu-id="c619d-142">Computer Supportmitarbeiter können eine Remote Desktop Sitzung anzeigen und steuern.</span><span class="sxs-lookup"><span data-stu-id="c619d-142">Computer support staff can view and control a remote desktop session.</span></span> <span data-ttu-id="c619d-143">Das Freigeben von Eingabe-und Anzeige Grafiken zwischen zwei Remote Desktop Sitzungen bietet einem Supportmitarbeiter die Möglichkeit, Probleme Remote zu diagnostizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="c619d-143">Sharing input and display graphics between two remote desktop sessions gives a support person the ability to diagnose and resolve problems remotely.</span></span>

</dd> <dt>

<span data-ttu-id="c619d-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Netzwerk Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="c619d-144"><span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Network load balancing</span></span>
</dt> <dd>

<span data-ttu-id="c619d-145">RDP nutzt den Netzwerk Lastenausgleich (Network Load Balancing, NLB), sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c619d-145">RDP takes advantage of network load balancing (NLB), where available.</span></span>

</dd> </dl>

<span data-ttu-id="c619d-146">Darüber hinaus enthält RDP die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="c619d-146">In addition, RDP contains the following features:</span></span>

-   <span data-ttu-id="c619d-147">Unterstützung für 24-Bit-Farben.</span><span class="sxs-lookup"><span data-stu-id="c619d-147">Support for 24-bit color.</span></span>
-   <span data-ttu-id="c619d-148">Verbesserte Leistung gegenüber niedriger Geschwindigkeit bei DFÜ-Verbindungen durch reduzierte Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="c619d-148">Improved performance over low-speed dial-up connections through reduced bandwidth.</span></span>
-   <span data-ttu-id="c619d-149">Smartcardauthentifizierung über Remotedesktopdienste.</span><span class="sxs-lookup"><span data-stu-id="c619d-149">Smart Card authentication through Remote Desktop Services.</span></span>
-   <span data-ttu-id="c619d-150">Tastatur Einbindung.</span><span class="sxs-lookup"><span data-stu-id="c619d-150">Keyboard hooking.</span></span> <span data-ttu-id="c619d-151">Die Möglichkeit, spezielle Windows-Tastenkombinationen im Vollbildmodus an den lokalen Computer oder einen Remote Computer weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="c619d-151">The ability to direct special Windows key combinations, in full-screen mode, to the local computer or to a remote computer.</span></span>
-   <span data-ttu-id="c619d-152">Audio-, Laufwerk-, Port-und Netzwerkdrucker Umleitung.</span><span class="sxs-lookup"><span data-stu-id="c619d-152">Sound, drive, port, and network printer redirection.</span></span> <span data-ttu-id="c619d-153">Sounds, die auf dem Remote Computer auftreten, können auf dem Client Computer, auf dem der RDC-Client ausgeführt wird, und lokale Client Laufwerke für die Remote Desktop Sitzung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c619d-153">Sounds that occur on the remote computer can be heard on the client computer running the RDC client, and local client drives will be visible to the remote desktop session.</span></span>

 

 