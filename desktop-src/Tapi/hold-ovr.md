---
description: Der Hold-Vorgang ermöglicht es einer einzelnen Adresse, mehrere Kommunikationssitzungen zu verarbeiten.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Aufbewahrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afacd6d9664e9a095a1e8b0c725dc0171da709fdecffb88b428231a5b5359a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003638"
---
# <a name="hold"></a>Aufbewahrung

Der Hold-Vorgang ermöglicht es einer einzelnen Adresse, mehrere Kommunikationssitzungen zu verarbeiten. Durch das Platzieren einer Sitzung in einer hard hold-Einstellung wird die Zeile/Adresse des Benutzers für andere Aufrufe frei. Ein Aufruf von Hard Hold kann in der Regel nicht übertragen oder in einen Telefonkonferenzsaufruf eingeschlossen werden, aber ein Telefonanruf ist möglich. Telefonkonferenzen werden mithilfe von [Konferenz- oder](conference-ovr.md) [Übertragungsvorgängen](transfer-ovr.md) initiiert.

Nachdem ein Aufruf erfolgreich zurückgehalten wurde, geht der Aufrufzustand in der Regel in den Zustand "Einbehaltung" über. Während ein Aufruf zurück gehalten wird, kann die Anwendung Nachrichten zu Zustandsänderungen des gehaltenen Aufrufs empfangen. Wenn die gehaltene Partei z. B. nicht mehr aufhängt, kann der Aufrufzustand in getrennt überwechseln.

In einer Überbrückungssituation wird der Aufruf möglicherweise nicht tatsächlich durch den Haltevorgang zurückhalten. Der Status anderer Stationen im Anruf kann steuern (z. B. der Versuch, einen Anruf zu "halten", wenn andere Stationen teilnehmen, ist nicht möglich). Stattdessen kann der Aufruf einfach in den inaktiven Zustand geändert werden, während er an anderen Stationen verbunden bleibt.

Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.

**TAPI 2.x:** Siehe [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).

**TAPI 3.x:** Weitere Informationen [**finden Sie unter ITBasicCallControl::Hold.**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold)

 

 
