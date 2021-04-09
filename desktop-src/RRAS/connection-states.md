---
title: Verbindungszustände
description: Beim Herstellen einer Verbindung mit einem Remote Server führen der RAS-Verbindungs-Manager und der RAS-Server auf dem Remote Computer mehrere Schritte aus, um die Verbindung herzustellen.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4488cc020a8a1b2a7da93384a4a5be1edb5182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858365"
---
# <a name="connection-states"></a><span data-ttu-id="6060b-103">Verbindungszustände</span><span class="sxs-lookup"><span data-stu-id="6060b-103">Connection States</span></span>

<span data-ttu-id="6060b-104">Beim Herstellen einer Verbindung mit einem Remote Server führen der RAS-Verbindungs-Manager und der RAS-Server auf dem Remote Computer mehrere Schritte aus, um die Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="6060b-104">During the process of connecting to a remote server, the Remote Access Connection Manager and the RAS server on the remote computer perform several steps to establish the connection.</span></span> <span data-ttu-id="6060b-105">Jeder dieser Schritte wird durch einen Verbindungsstatus identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6060b-105">Each of these steps is identified by a connection state.</span></span> <span data-ttu-id="6060b-106">Die [**raskonnstate**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) -Enumeration ist ein Satz von Werten, die diesen Verbindungs Zuständen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6060b-106">The [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumeration is a set of values that correspond to these connection states.</span></span> <span data-ttu-id="6060b-107">Die Verbindungszustände können in die folgenden drei Gruppen unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="6060b-107">The connection states can be divided into the following three groups:</span></span>

<dl> <dt>

<span data-ttu-id="6060b-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Ausführen von Zuständen</span><span class="sxs-lookup"><span data-stu-id="6060b-108"><span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Running states</span></span>
</dt> <dd>

<span data-ttu-id="6060b-109">Die laufenden Zustände sind die Teile des Verbindungs Vorgangs, die RAS automatisch verarbeitet, z. b. das Herstellen einer Verbindung mit den erforderlichen Geräten, das Authentifizieren des Benutzers und das warten auf einen Rückruf vom Remote Server.</span><span class="sxs-lookup"><span data-stu-id="6060b-109">The running states are the parts of the connection operation that RAS handles automatically, such as connecting to the necessary devices, authenticating the user, and waiting for a callback from the remote server.</span></span> <span data-ttu-id="6060b-110">Wenn kein Fehler auftritt, muss der RAS-Client keine Aktion durchführen, außer um die Benachrichtigung an den Benutzer zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="6060b-110">Unless an error occurs, the RAS client need take no action other than to pass the notification on to the user.</span></span>

</dd> <dt>

<span data-ttu-id="6060b-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Angehaltene Zustände</span><span class="sxs-lookup"><span data-stu-id="6060b-111"><span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Paused states</span></span>
</dt> <dd>

<span data-ttu-id="6060b-112">Die [angehaltenen Zustände](paused-states.md) treten auf, wenn der Remote Server den Verbindungsvorgang anhält, um zusätzliche Eingaben vom Benutzer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6060b-112">The [paused states](paused-states.md) occur when the remote server pauses the connection operation to get additional input from the user.</span></span> <span data-ttu-id="6060b-113">Während eines angehaltenen Zustands kann der Benutzer eine [Rückruf](callback-connections.md) Nummer, einen anderen Benutzernamen und ein Kennwort eingeben, wenn die Benutzerauthentifizierung fehlschlägt, oder ein neues Kennwort, wenn das alte Kennwort abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="6060b-113">During a paused state, the user can type a [callback](callback-connections.md) number, a different user name and password if the user authentication fails, or a new password if the old one has expired.</span></span>

</dd> <dt>

<span data-ttu-id="6060b-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal Zustände</span><span class="sxs-lookup"><span data-stu-id="6060b-114"><span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal states</span></span>
</dt> <dd>

<span data-ttu-id="6060b-115">Die Terminal Zustände treten auf, wenn die Verbindung erfolgreich hergestellt wurde, der Verbindungsvorgang fehlgeschlagen ist oder die Verbindung durch einen [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) -Befehl getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="6060b-115">The terminal states occur when the connection has been successfully established, the connection operation has failed, or the connection has been broken by a [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) call.</span></span>

</dd> </dl>

<span data-ttu-id="6060b-116">Es gibt mehrere Mechanismen, die ein RAS-Client verwenden kann, um den aktuellen Status eines Verbindungs Vorgangs zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="6060b-116">There are several mechanisms that a RAS client can use to determine the current state of a connection operation.</span></span> <span data-ttu-id="6060b-117">Wenn ein RAS-Client die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " asynchron ausführt, sendet der RAS-Verbindungs-Manager bei jeder Änderung des Verbindungs Zustands Status Benachrichtigungen an den [Benachrichtigungs Handler](notification-handlers.md) des Clients.</span><span class="sxs-lookup"><span data-stu-id="6060b-117">When a RAS client executes the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function asynchronously, the Remote Access Connection Manager sends progress notifications to the client's [notification handler](notification-handlers.md) whenever the connection state changes.</span></span> <span data-ttu-id="6060b-118">Außerdem kann der Client die Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " verwenden, um den aktuellen Zustand eines beliebigen RAS-Verbindungs Vorgangs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6060b-118">In addition, the client can use the [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) function to get the current state of any RAS connection operation.</span></span>

 

 