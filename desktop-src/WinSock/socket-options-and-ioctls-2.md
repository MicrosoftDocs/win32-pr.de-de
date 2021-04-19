---
description: Einige der Socketoptionen für Windows Sockets 2 werden in der folgenden Tabelle zusammengefasst.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Socketoptionen und IOCTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362382"
---
# <a name="socket-options-and-ioctls"></a><span data-ttu-id="32fbd-103">Socketoptionen und IOCTLs</span><span class="sxs-lookup"><span data-stu-id="32fbd-103">Socket Options and IOCTLs</span></span>

<span data-ttu-id="32fbd-104">Einige der Socketoptionen für Windows Sockets 2 werden in der folgenden Tabelle zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="32fbd-104">Some of the socket options for Windows Sockets 2 are summarized in the following table.</span></span> <span data-ttu-id="32fbd-105">Ausführlichere Informationen finden Sie in Abschnitt 4 unter [**wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) und/oder [**wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="32fbd-105">More detailed information is provided in section 4 under [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span></span> <span data-ttu-id="32fbd-106">Weitere neue Protokoll spezifische Socketoptionen finden Sie in der Protocol-Specific-Anlage.</span><span class="sxs-lookup"><span data-stu-id="32fbd-106">There are other new protocol-specific socket options which can be found in the Protocol-Specific Annex.</span></span> <span data-ttu-id="32fbd-107">Eine komplette Liste der [**Socketoptionen**](socket-options.md) für Windows Sockets finden Sie in der Winsock-Referenz.</span><span class="sxs-lookup"><span data-stu-id="32fbd-107">A complete list of [**Socket Options**](socket-options.md) for Windows Sockets are available in the Winsock reference.</span></span>

<span data-ttu-id="32fbd-108">Eine Zusammenfassung der Winsock IOCTLs finden Sie unter [Zusammenfassung der socketioctl-Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span><span class="sxs-lookup"><span data-stu-id="32fbd-108">For a a summary of some of the Winsock Ioctls, see [Summary of Socket Ioctl Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span></span> <span data-ttu-id="32fbd-109">Eine komplette Liste der [**Winsock IOCTLs**](winsock-ioctls.md) finden Sie in der Winsock-Referenz.</span><span class="sxs-lookup"><span data-stu-id="32fbd-109">A complete list of [**Winsock IOCTLs**](winsock-ioctls.md) are available in the Winsock reference.</span></span>

## <a name="summary-of-common-socket-options"></a><span data-ttu-id="32fbd-110">Zusammenfassung allgemeiner Socketoptionen</span><span class="sxs-lookup"><span data-stu-id="32fbd-110">Summary of Common Socket Options</span></span>

<span data-ttu-id="32fbd-111">Ein Winsock-Dienstanbieter muss alle diese Optionen erkennen, und (für [**wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) gibt für jeden eine plausible Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="32fbd-111">A Winsock service provider must recognize all of these options, and (for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) return plausible values for each.</span></span> <span data-ttu-id="32fbd-112">Der Standardwert für jede Option ist in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="32fbd-112">The default value for each option is shown in the following table.</span></span>

<span data-ttu-id="32fbd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="32fbd-113">Value</span></span>

<span data-ttu-id="32fbd-114">type</span><span class="sxs-lookup"><span data-stu-id="32fbd-114">Type</span></span>

<span data-ttu-id="32fbd-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="32fbd-115">Meaning</span></span>

<span data-ttu-id="32fbd-116">Standard</span><span class="sxs-lookup"><span data-stu-id="32fbd-116">Default</span></span>

<span data-ttu-id="32fbd-117">Hinweis</span><span class="sxs-lookup"><span data-stu-id="32fbd-117">Note</span></span>

<span data-ttu-id="32fbd-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>also \_ akzeptconn</span><span class="sxs-lookup"><span data-stu-id="32fbd-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO\_ACCEPTCONN</span></span>

<span data-ttu-id="32fbd-119">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-119">BOOL</span></span>

<span data-ttu-id="32fbd-120">Der Socket lauscht.</span><span class="sxs-lookup"><span data-stu-id="32fbd-120">Socket is listening.</span></span>

<span data-ttu-id="32fbd-121">FALSE, es sei denn, ein [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) wurde ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="32fbd-121">FALSE unless a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) has been performed.</span></span>

<span data-ttu-id="32fbd-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>also \_ Broadcast</span><span class="sxs-lookup"><span data-stu-id="32fbd-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO\_BROADCAST</span></span>

<span data-ttu-id="32fbd-123">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-123">BOOL</span></span>

<span data-ttu-id="32fbd-124">Socket ist für die Übertragung und den Empfang von Broadcast Nachrichten konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="32fbd-124">Socket is configured for the transmission and receipt of broadcast messages.</span></span>

<span data-ttu-id="32fbd-125">false</span><span class="sxs-lookup"><span data-stu-id="32fbd-125">FALSE</span></span>

<span data-ttu-id="32fbd-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>also \_ Debuggen</span><span class="sxs-lookup"><span data-stu-id="32fbd-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>SO\_DEBUG</span></span>

<span data-ttu-id="32fbd-127">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-127">BOOL</span></span>

<span data-ttu-id="32fbd-128">Debuggen ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="32fbd-128">Debugging is enabled.</span></span>

<span data-ttu-id="32fbd-129">false</span><span class="sxs-lookup"><span data-stu-id="32fbd-129">FALSE</span></span>

<span data-ttu-id="32fbd-130">Ich</span><span class="sxs-lookup"><span data-stu-id="32fbd-130">(i)</span></span>

<span data-ttu-id="32fbd-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DontLinger</span><span class="sxs-lookup"><span data-stu-id="32fbd-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>SO\_DONTLINGER</span></span>

<span data-ttu-id="32fbd-132">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-132">BOOL</span></span>

<span data-ttu-id="32fbd-133">True gibt an, dass die \_ Option so LINGER deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="32fbd-133">If true, the SO\_LINGER option is disabled.</span></span>

<span data-ttu-id="32fbd-134">TRUE</span><span class="sxs-lookup"><span data-stu-id="32fbd-134">TRUE</span></span>

<span data-ttu-id="32fbd-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO \_ DontRoute</span><span class="sxs-lookup"><span data-stu-id="32fbd-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO\_DONTROUTE</span></span>

<span data-ttu-id="32fbd-136">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-136">BOOL</span></span>

<span data-ttu-id="32fbd-137">Das Routing ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="32fbd-137">Routing is disabled.</span></span> <span data-ttu-id="32fbd-138">Ist erfolgreich, wird aber bei AF \_ inet Sockets ignoriert; schlägt bei AF \_ inet6 Sockets mit [wsakooprodeopt](windows-sockets-error-codes-2.md)fehl.</span><span class="sxs-lookup"><span data-stu-id="32fbd-138">Succeeds but is ignored on AF\_INET sockets; fails on AF\_INET6 sockets with [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="32fbd-139">Wird nicht für ATM-Sockets unterstützt (führt zu einem Fehler).</span><span class="sxs-lookup"><span data-stu-id="32fbd-139">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="32fbd-140">false</span><span class="sxs-lookup"><span data-stu-id="32fbd-140">FALSE</span></span>

<span data-ttu-id="32fbd-141">Ich</span><span class="sxs-lookup"><span data-stu-id="32fbd-141">(i)</span></span>

<span data-ttu-id="32fbd-142"><span id="SO_ERROR"></span><span id="so_error"></span>\_Fehler</span><span class="sxs-lookup"><span data-stu-id="32fbd-142"><span id="SO_ERROR"></span><span id="so_error"></span>SO\_ERROR</span></span>

<span data-ttu-id="32fbd-143">INT</span><span class="sxs-lookup"><span data-stu-id="32fbd-143">int</span></span>

<span data-ttu-id="32fbd-144">Ruft den Fehlerstatus ab und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="32fbd-144">Retrieves error status and clear.</span></span>

<span data-ttu-id="32fbd-145">0</span><span class="sxs-lookup"><span data-stu-id="32fbd-145">0</span></span>

<span data-ttu-id="32fbd-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_Gruppen- \_ ID</span><span class="sxs-lookup"><span data-stu-id="32fbd-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO\_GROUP\_ID</span></span>

<span data-ttu-id="32fbd-147">GROUP</span><span class="sxs-lookup"><span data-stu-id="32fbd-147">GROUP</span></span>

<span data-ttu-id="32fbd-148">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="32fbd-148">Reserved.</span></span>

<span data-ttu-id="32fbd-149">NULL</span><span class="sxs-lookup"><span data-stu-id="32fbd-149">NULL</span></span>

<span data-ttu-id="32fbd-150">Nur Get</span><span class="sxs-lookup"><span data-stu-id="32fbd-150">Get only</span></span>

<span data-ttu-id="32fbd-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_Gruppen \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="32fbd-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO\_GROUP\_PRIORITY</span></span>

<span data-ttu-id="32fbd-152">INT</span><span class="sxs-lookup"><span data-stu-id="32fbd-152">int</span></span>

<span data-ttu-id="32fbd-153">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="32fbd-153">Reserved.</span></span>

<span data-ttu-id="32fbd-154">0</span><span class="sxs-lookup"><span data-stu-id="32fbd-154">0</span></span>

[<span data-ttu-id="32fbd-155">**\_KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="32fbd-155">**SO\_KEEPALIVE**</span></span>](so-keepalive.md)

<span data-ttu-id="32fbd-156">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-156">BOOL</span></span>

<span data-ttu-id="32fbd-157">Keepalives werden gesendet.</span><span class="sxs-lookup"><span data-stu-id="32fbd-157">Keepalives are being sent.</span></span> <span data-ttu-id="32fbd-158">Wird nicht für ATM-Sockets unterstützt (führt zu einem Fehler).</span><span class="sxs-lookup"><span data-stu-id="32fbd-158">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="32fbd-159">false</span><span class="sxs-lookup"><span data-stu-id="32fbd-159">FALSE</span></span>

<span data-ttu-id="32fbd-160">Ich</span><span class="sxs-lookup"><span data-stu-id="32fbd-160">(i)</span></span>

<span data-ttu-id="32fbd-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO \_ LINGER</span><span class="sxs-lookup"><span data-stu-id="32fbd-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO\_LINGER</span></span>

<span data-ttu-id="32fbd-162">Struktur-Linger</span><span class="sxs-lookup"><span data-stu-id="32fbd-162">Structure linger</span></span>

<span data-ttu-id="32fbd-163">Gibt die aktuellen Linger-Optionen zurück.</span><span class="sxs-lookup"><span data-stu-id="32fbd-163">Returns the current linger options.</span></span>

<span data-ttu-id="32fbd-164">l \_ ToggleMicrophoneOnOff ist 0</span><span class="sxs-lookup"><span data-stu-id="32fbd-164">l\_onoff is 0</span></span>

<span data-ttu-id="32fbd-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_Maximale Nachrichten \_ \_ Größe</span><span class="sxs-lookup"><span data-stu-id="32fbd-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO\_MAX\_MSG\_SIZE</span></span>

<span data-ttu-id="32fbd-166">INT</span><span class="sxs-lookup"><span data-stu-id="32fbd-166">int</span></span>

<span data-ttu-id="32fbd-167">Maximale ausgehende Größe einer Nachricht für Nachrichten sockettypen.</span><span class="sxs-lookup"><span data-stu-id="32fbd-167">Maximum outbound size of a message for message socket types.</span></span> <span data-ttu-id="32fbd-168">Es gibt keine Bereitstellung, um die maximale Größe eingehender Nachrichten zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="32fbd-168">There is no provision to determine the maximum inbound message size.</span></span> <span data-ttu-id="32fbd-169">Hat keine Bedeutung für Datenstrom orientierte Sockets.</span><span class="sxs-lookup"><span data-stu-id="32fbd-169">Has no meaning for stream-oriented sockets.</span></span>

<span data-ttu-id="32fbd-170">Implementierungsabhängig</span><span class="sxs-lookup"><span data-stu-id="32fbd-170">Implementation dependent</span></span>

<span data-ttu-id="32fbd-171">Nur Get</span><span class="sxs-lookup"><span data-stu-id="32fbd-171">Get only</span></span>

<span data-ttu-id="32fbd-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_oobinline</span><span class="sxs-lookup"><span data-stu-id="32fbd-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO\_OOBINLINE</span></span>

<span data-ttu-id="32fbd-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-173">BOOL</span></span>

<span data-ttu-id="32fbd-174">OOB-Daten werden im normalen Datenstrom empfangen.</span><span class="sxs-lookup"><span data-stu-id="32fbd-174">OOB data is being received in the normal data stream.</span></span>

<span data-ttu-id="32fbd-175">false</span><span class="sxs-lookup"><span data-stu-id="32fbd-175">FALSE</span></span>

<span data-ttu-id="32fbd-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_Protokoll \_ infow</span><span class="sxs-lookup"><span data-stu-id="32fbd-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO\_PROTOCOL\_INFOW</span></span>

<span data-ttu-id="32fbd-177">[ **wsaprotocol-Struktur \_ Informationen**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span><span class="sxs-lookup"><span data-stu-id="32fbd-177">structure [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span></span>

<span data-ttu-id="32fbd-178">Beschreibung der Protokollinformationen für das Protokoll, das an diesen Socket gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="32fbd-178">Description of protocol information for the protocol that is bound to this socket.</span></span>

<span data-ttu-id="32fbd-179">Protokoll abhängig</span><span class="sxs-lookup"><span data-stu-id="32fbd-179">Protocol dependent</span></span>

<span data-ttu-id="32fbd-180">Nur Get</span><span class="sxs-lookup"><span data-stu-id="32fbd-180">Get only</span></span>

<span data-ttu-id="32fbd-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_rcvbuf</span><span class="sxs-lookup"><span data-stu-id="32fbd-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO\_RCVBUF</span></span>

<span data-ttu-id="32fbd-182">INT</span><span class="sxs-lookup"><span data-stu-id="32fbd-182">int</span></span>

<span data-ttu-id="32fbd-183">Der gesamte pro-Socket-Pufferspeicher, der für Empfangs Vorgänge reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="32fbd-183">The total per-socket buffer space reserved for receives.</span></span> <span data-ttu-id="32fbd-184">Dies steht in keinem Zusammenhang mit \_ der maximalen Nachrichten \_ \_ Größe und entspricht nicht notwendigerweise der Größe des TCP-Empfangs Fensters.</span><span class="sxs-lookup"><span data-stu-id="32fbd-184">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of the TCP receive window.</span></span>

<span data-ttu-id="32fbd-185">Implementierungsabhängig</span><span class="sxs-lookup"><span data-stu-id="32fbd-185">Implementation dependent</span></span>

<span data-ttu-id="32fbd-186">Ich</span><span class="sxs-lookup"><span data-stu-id="32fbd-186">(i)</span></span>

<span data-ttu-id="32fbd-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_reuseaddr</span><span class="sxs-lookup"><span data-stu-id="32fbd-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO\_REUSEADDR</span></span>

<span data-ttu-id="32fbd-188">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-188">BOOL</span></span>

<span data-ttu-id="32fbd-189">Die Adresse, an die dieser Socket gebunden ist, kann von anderen Benutzern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="32fbd-189">The address to which this socket is bound can be used by others.</span></span> <span data-ttu-id="32fbd-190">Gilt nicht für ATM-Sockets.</span><span class="sxs-lookup"><span data-stu-id="32fbd-190">Not applicable on ATM sockets.</span></span>

<span data-ttu-id="32fbd-191">false</span><span class="sxs-lookup"><span data-stu-id="32fbd-191">FALSE</span></span>

<span data-ttu-id="32fbd-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_sndbuf</span><span class="sxs-lookup"><span data-stu-id="32fbd-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO\_SNDBUF</span></span>

<span data-ttu-id="32fbd-193">INT</span><span class="sxs-lookup"><span data-stu-id="32fbd-193">int</span></span>

<span data-ttu-id="32fbd-194">Der Gesamt Puffer Speicherplatz pro Socket, der für Sende Vorgänge reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="32fbd-194">The total per-socket buffer space reserved for sends.</span></span> <span data-ttu-id="32fbd-195">Dies steht in keinem Zusammenhang mit \_ der maximalen Nachrichten \_ \_ Größe und entspricht nicht notwendigerweise der Größe eines TCP-Sende Fensters.</span><span class="sxs-lookup"><span data-stu-id="32fbd-195">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of a TCP send window.</span></span>

<span data-ttu-id="32fbd-196">Implementierungsabhängig</span><span class="sxs-lookup"><span data-stu-id="32fbd-196">Implementation dependent</span></span>

<span data-ttu-id="32fbd-197">Ich</span><span class="sxs-lookup"><span data-stu-id="32fbd-197">(i)</span></span>

<span data-ttu-id="32fbd-198"><span id="SO_TYPE"></span><span id="so_type"></span>\_Typ</span><span class="sxs-lookup"><span data-stu-id="32fbd-198"><span id="SO_TYPE"></span><span id="so_type"></span>SO\_TYPE</span></span>

<span data-ttu-id="32fbd-199">INT</span><span class="sxs-lookup"><span data-stu-id="32fbd-199">int</span></span>

<span data-ttu-id="32fbd-200">Der Typ des Sockets (z. b. sock- \_ Stream).</span><span class="sxs-lookup"><span data-stu-id="32fbd-200">The type of the socket (for example, SOCK\_STREAM).</span></span>

<span data-ttu-id="32fbd-201">Wie durch Socket erstellt.</span><span class="sxs-lookup"><span data-stu-id="32fbd-201">As created through socket.</span></span>

<span data-ttu-id="32fbd-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD- \_ Konfiguration</span><span class="sxs-lookup"><span data-stu-id="32fbd-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD\_CONFIG</span></span>

<span data-ttu-id="32fbd-203">char-weit \*</span><span class="sxs-lookup"><span data-stu-id="32fbd-203">char FAR \*</span></span>

<span data-ttu-id="32fbd-204">Ein undurchsichtiges Datenstruktur Objekt, das Konfigurationsinformationen des Dienstanbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="32fbd-204">An opaque data structure object containing configuration information of the service provider.</span></span>

<span data-ttu-id="32fbd-205">Implementierungsabhängig</span><span class="sxs-lookup"><span data-stu-id="32fbd-205">Implementation dependent</span></span>

<span data-ttu-id="32fbd-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP- \_ nodelay</span><span class="sxs-lookup"><span data-stu-id="32fbd-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP\_NODELAY</span></span>

<span data-ttu-id="32fbd-207">BOOL</span><span class="sxs-lookup"><span data-stu-id="32fbd-207">BOOL</span></span>

<span data-ttu-id="32fbd-208">Deaktiviert den Nagle-Algorithmus für Sammelsendungen.</span><span class="sxs-lookup"><span data-stu-id="32fbd-208">Disables the Nagle algorithm for send coalescing.</span></span>

<span data-ttu-id="32fbd-209">Implementierungsabhängig</span><span class="sxs-lookup"><span data-stu-id="32fbd-209">Implementation dependent</span></span>

<span data-ttu-id="32fbd-210">(i) ein Dienstanbieter kann diese Option auf [**wspsetsockopt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) im Hintergrund ignorieren und einen konstanten Wert für [**wspgetsockopt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))zurückgeben. er kann auch einen Wert für **wspsetsockopt** annehmen und den entsprechenden Wert in **wspgetsockopt** zurückgeben, ohne den Wert zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="32fbd-210">(i) A service provider may silently ignore this option on [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) and return a constant value for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), or it may accept a value for **WSPSetSockOpt** and return the corresponding value in **WSPGetSockOpt** without using the value in any way.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="32fbd-211">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32fbd-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32fbd-212">**Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="32fbd-212">**Socket Options**</span></span>](socket-options.md)
</dt> <dt>

[<span data-ttu-id="32fbd-213">**Optionen des Sol- \_ socketsockets**</span><span class="sxs-lookup"><span data-stu-id="32fbd-213">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="32fbd-214">**Ipproto \_ TCP-Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="32fbd-214">**IPPROTO\_TCP Socket Options**</span></span>](ipproto-tcp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="32fbd-215">**Ipproto \_ UDP-Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="32fbd-215">**IPPROTO\_UDP Socket Options**</span></span>](ipproto-udp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="32fbd-216">**Winsock IOCTLs**</span><span class="sxs-lookup"><span data-stu-id="32fbd-216">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
