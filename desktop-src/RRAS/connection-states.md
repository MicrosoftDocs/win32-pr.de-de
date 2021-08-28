---
title: Verbindungszustände
description: Während der Verbindungsherstellung mit einem Remoteserver führen die Remotezugriffs-Verbindungs-Manager und der RAS-Server auf dem Remotecomputer mehrere Schritte aus, um die Verbindung herzustellen.
ms.assetid: 7a8b0086-308b-47d2-888e-69ff473c6015
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9e52e1e4ea4a071f6606681aa2dc2fc15e88df659f8fd16746abf2d84727d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074220"
---
# <a name="connection-states"></a>Verbindungszustände

Während der Verbindungsherstellung mit einem Remoteserver führen die Remotezugriffs-Verbindungs-Manager und der RAS-Server auf dem Remotecomputer mehrere Schritte aus, um die Verbindung herzustellen. Jeder dieser Schritte wird durch einen Verbindungsstatus identifiziert. Die [**RASCONNSTATE-Enumeration**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) ist ein Satz von Werten, die diesen Verbindungszuständen entsprechen. Die Verbindungszustände können in die folgenden drei Gruppen unterteilt werden:

<dl> <dt>

<span id="Running_states"></span><span id="running_states"></span><span id="RUNNING_STATES"></span>Ausführungszustände
</dt> <dd>

Die Ausführungszustände sind die Teile des Verbindungsvorgangs, die RAS automatisch verarbeitet, z. B. das Herstellen einer Verbindung mit den erforderlichen Geräten, das Authentifizieren des Benutzers und das Warten auf einen Rückruf vom Remoteserver. Sofern kein Fehler auftritt, muss der RAS-Client keine andere Aktion als ergreifen, um die Benachrichtigung an den Benutzer weiterzuleiten.

</dd> <dt>

<span id="Paused_states"></span><span id="paused_states"></span><span id="PAUSED_STATES"></span>Angehaltene Zustände
</dt> <dd>

Die [angehaltenen Zustände](paused-states.md) treten auf, wenn der Remoteserver den Verbindungsvorgang angibt, um zusätzliche Eingaben vom Benutzer zu erhalten. Während eines angehaltenen Zustands kann der Benutzer eine [Rückrufnummer,](callback-connections.md) einen anderen Benutzernamen und ein anderes Kennwort eingeben, wenn die Benutzerauthentifizierung fehlschlägt, oder ein neues Kennwort, wenn das alte abgelaufen ist.

</dd> <dt>

<span id="Terminal_states"></span><span id="terminal_states"></span><span id="TERMINAL_STATES"></span>Terminalzustände
</dt> <dd>

Die Terminalzustände treten auf, wenn die Verbindung erfolgreich hergestellt wurde, der Verbindungsvorgang fehlgeschlagen ist oder die Verbindung durch einen [**RasHangUp-Aufruf**](/windows/desktop/api/Ras/nf-ras-rashangupa) unterbrochen wurde.

</dd> </dl>

Es gibt mehrere Mechanismen, mit denen ein RAS-Client den aktuellen Status eines Verbindungsvorgangs bestimmen kann. Wenn ein RAS-Client die [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchron ausführt, sendet der Remotezugriffs-Verbindungs-Manager Statusbenachrichtigungen an den [Benachrichtigungshandler](notification-handlers.md) des Clients, wenn sich der Verbindungszustand ändert. Darüber hinaus kann der Client die [**RasGetConnectStatus-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) verwenden, um den aktuellen Zustand eines beliebigen RAS-Verbindungsvorgangs abzurufen.

 

 