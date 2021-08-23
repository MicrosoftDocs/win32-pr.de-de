---
title: Serveranwendung für virtuelle Kanäle
description: Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Anwendung im Benutzermodus sein, die in einer Clientsitzung auf dem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) ausgeführt wird. Beachten Sie, dass Sie eine Methode angeben müssen, um die Serveranwendung zu starten.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d63a758f4860a0ab606f18c4a5086d305b1f627475bf7bab588648cea8aabd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423563"
---
# <a name="virtual-channel-server-application"></a>Serveranwendung für virtuelle Kanäle

Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Anwendung im Benutzermodus sein, die in einer Clientsitzung auf dem Remotedesktop-Sitzungshost -Server (RD-Sitzungshost) ausgeführt wird. Beachten Sie, dass Sie eine Methode angeben müssen, um die Serveranwendung zu starten. Sie können dies auf verschiedene Weise erreichen. Beispielsweise können Sie ein Anmeldeskript oder ein Programm oder Skript im Ordner Start verwenden. Benutzer können die Anwendung auch starten.

Sie müssen den Namen der Virtuellen Kanalserveranwendung in der Registrierung speichern, indem Sie unter dem folgenden Speicherort einen Unterschlüssel hinzufügen:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminal Server** \\ **Addins**

Weitere Informationen zum Unterschlüssel finden Sie unter [Überwachen von Sitzungsverbindungen und Trennungen.](monitoring-session-connections-and-disconnections.md)

Die Serveranwendung kann die [**WTSVirtualChannelOpen-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) aufrufen, um ein Handle für einen virtuellen Kanal zu öffnen. Die Anwendung kann dann das Handle in einer der folgenden Funktionen verwenden.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Schließt ein geöffnetes Handle für virtuelle Kanäle.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Löscht alle Eingabedaten in der Warteschlange, die vom Client an den Server auf einem bestimmten virtuellen Kanal gesendet werden.

> [!Note]  
> Diese Funktion wird derzeit nicht von Remotedesktopdienste verwendet.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Löscht alle Ausgabedaten in der Warteschlange, die vom Server an den Client in einem bestimmten virtuellen Kanal gesendet werden.

> [!Note]  
> Diese Funktion wird derzeit nicht von Remotedesktopdienste verwendet.

 

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Gibt Informationen zu einem angegebenen virtuellen Kanal zurück.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Liest Daten vom Serverende eines virtuellen Kanals.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Schreibt Daten in das Serverende eines virtuellen Kanals.

</dd> </dl>

 

 




