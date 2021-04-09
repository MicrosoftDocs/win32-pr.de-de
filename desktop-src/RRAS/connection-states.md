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
# <a name="connection-states"></a>Verbindungszustände

Beim Herstellen einer Verbindung mit einem Remote Server führen der RAS-Verbindungs-Manager und der RAS-Server auf dem Remote Computer mehrere Schritte aus, um die Verbindung herzustellen. Jeder dieser Schritte wird durch einen Verbindungsstatus identifiziert. Die [**raskonnstate**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) -Enumeration ist ein Satz von Werten, die diesen Verbindungs Zuständen entsprechen. Die Verbindungszustände können in die folgenden drei Gruppen unterteilt werden:

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Ausführen von Zuständen
</dt> <dd>

Die laufenden Zustände sind die Teile des Verbindungs Vorgangs, die RAS automatisch verarbeitet, z. b. das Herstellen einer Verbindung mit den erforderlichen Geräten, das Authentifizieren des Benutzers und das warten auf einen Rückruf vom Remote Server. Wenn kein Fehler auftritt, muss der RAS-Client keine Aktion durchführen, außer um die Benachrichtigung an den Benutzer zu übergeben.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Angehaltene Zustände
</dt> <dd>

Die [angehaltenen Zustände](paused-states.md) treten auf, wenn der Remote Server den Verbindungsvorgang anhält, um zusätzliche Eingaben vom Benutzer zu erhalten. Während eines angehaltenen Zustands kann der Benutzer eine [Rückruf](callback-connections.md) Nummer, einen anderen Benutzernamen und ein Kennwort eingeben, wenn die Benutzerauthentifizierung fehlschlägt, oder ein neues Kennwort, wenn das alte Kennwort abgelaufen ist.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminal Zustände
</dt> <dd>

Die Terminal Zustände treten auf, wenn die Verbindung erfolgreich hergestellt wurde, der Verbindungsvorgang fehlgeschlagen ist oder die Verbindung durch einen [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) -Befehl getrennt wurde.

</dd> </dl>

Es gibt mehrere Mechanismen, die ein RAS-Client verwenden kann, um den aktuellen Status eines Verbindungs Vorgangs zu bestimmen. Wenn ein RAS-Client die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " asynchron ausführt, sendet der RAS-Verbindungs-Manager bei jeder Änderung des Verbindungs Zustands Status Benachrichtigungen an den [Benachrichtigungs Handler](notification-handlers.md) des Clients. Außerdem kann der Client die Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " verwenden, um den aktuellen Zustand eines beliebigen RAS-Verbindungs Vorgangs zu erhalten.

 

 