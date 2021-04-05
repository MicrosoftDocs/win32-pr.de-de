---
title: Virtual Channel-Server Anwendung
description: Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Benutzermodusanwendung sein, die in einer Client Sitzung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird. Beachten Sie, dass Sie eine Methode zum Starten der Serveranwendung bereitstellen müssen.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711412"
---
# <a name="virtual-channel-server-application"></a>Virtual Channel-Server Anwendung

Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Benutzermodusanwendung sein, die in einer Client Sitzung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird. Beachten Sie, dass Sie eine Methode zum Starten der Serveranwendung bereitstellen müssen. Dies kann auf verschiedene Weise erreicht werden: Beispielsweise können Sie ein Anmelde Skript oder ein Programm oder Skript im Startordner verwenden. Benutzer können die Anwendung auch starten.

Sie müssen den Namen der Virtual Channel-Serveranwendung in der Registrierung speichern, indem Sie einen Unterschlüssel unter folgendem Speicherort hinzufügen:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminal Server**- \\ **AddIns**

Weitere Informationen zum Unterschlüssel finden Sie unter über [Wachen von Sitzungs Verbindungen und Verbindungsunterbrechungen](monitoring-session-connections-and-disconnections.md).

Die Serveranwendung kann die [**WFS virtualchannelopen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) -Funktion zum Öffnen eines Handles für einen virtuellen Channel aufruft. Die Anwendung kann dann das Handle in einer der folgenden Funktionen verwenden.

<dl> <dt>

[**Wout virtualchannelclose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Schließt einen geöffneten virtuellen Kanal handle.

</dd> <dt>

[**WGs virtualchannelpurgeinput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Löscht alle in die Warteschlange eingereihten Eingabedaten, die vom Client an den Server in einem bestimmten virtuellen Kanal gesendet werden.

> [!Note]  
> Diese Funktion wird zurzeit nicht von Remotedesktopdienste verwendet.

 

</dd> <dt>

[**Wzvirtualchannelpurgeoutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Löscht alle in die Warteschlange eingereihten Ausgabedaten, die vom Server an den Client in einem bestimmten virtuellen Kanal gesendet werden.

> [!Note]  
> Diese Funktion wird zurzeit nicht von Remotedesktopdienste verwendet.

 

</dd> <dt>

[**Wout virtualchannelquery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Gibt Informationen zu einem angegebenen virtuellen Kanal zurück.

</dd> <dt>

[**Wout virtualchannelread**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Liest Daten vom Server Ende eines virtuellen Kanals.

</dd> <dt>

[**Wout virtualchannelwrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Schreibt Daten auf das Server Ende eines virtuellen Kanals.

</dd> </dl>

 

 




