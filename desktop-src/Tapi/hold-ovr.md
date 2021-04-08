---
description: Der Hold-Vorgang ermöglicht es einer einzelnen Adresse, mehrere Kommunikationssitzungen zu verarbeiten.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Aufbewahrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863231"
---
# <a name="hold"></a>Aufbewahrung

Der Hold-Vorgang ermöglicht es einer einzelnen Adresse, mehrere Kommunikationssitzungen zu verarbeiten. Durch das Platzieren einer Sitzung auf einer Festplatte wird die Zeile/Adresse des Benutzers für andere Anrufe freigegeben. Ein-aufruhalte kann in der Regel nicht übertragen oder in einen Konferenzgespräch eingeschlossen werden, aber ein Beratungsgespräch ist möglich. Beratungs Anrufe werden mithilfe von [Konferenz](conference-ovr.md) -oder [Übertragungs](transfer-ovr.md) Vorgängen initiiert.

Nachdem ein Anruf erfolgreich angehalten wurde, wechselt der Anrufstatus in der Regel in den OnHold-Status. Während ein-Rückruf aktiv ist, kann die Anwendung Nachrichten zu Zustandsänderungen des gehaltenen Aufrufes empfangen. Wenn die Partei beispielsweise angehalten wird, kann der Status des Aufrufes zu "getrennt" übergehen.

In einer überbrückten Situation wird der anhalte Vorgang durch den Hold-Vorgang möglicherweise nicht angehalten. Der Status anderer Stationen im-Befehl kann Steuern (z. b. Wenn Sie versuchen, einen-Befehl anzuhalten, wenn keine anderen Stationen teilnehmen); Stattdessen kann der-Befehl einfach in den inaktiven Zustand geändert werden, während er an anderen Stationen verbunden bleibt.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linehold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineunhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3. x:** Siehe [**itbasiccallcontrol:: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).

 

 
