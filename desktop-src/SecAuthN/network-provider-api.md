---
description: Ein Netzwerkanbieter ist eine DLL, mit der das Windows-Betriebssystem mit anderen Arten von Netzwerken interagieren kann, z. b. Novell. Es handelt sich um einen Client des Windows-WNET-Treibers.
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: Netzwerkanbieter-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368942"
---
# <a name="network-provider-api"></a>Netzwerkanbieter-API

Ein Netzwerkanbieter ist eine DLL, mit der das Windows-Betriebssystem mit anderen Arten von Netzwerken interagieren kann, z. b. Novell. Es handelt sich um einen Client des Windows-WNET-Treibers. Ein Netzwerkanbieter implementiert Netzwerk spezifische Aktionen (z. b. das Herstellen einer Verbindung) und macht eine gemeinsame Schnittstelle für Windows verfügbar. Diese Schnittstelle wird als Netzwerkanbieter-API bezeichnet und besteht aus Funktionen, die vom Netzwerkanbieter implementiert werden. Sie können eine Netzwerkanbieter-dll erstellen, um neue Netzwerkprotokolle zu unterstützen.

Da jedes Netzwerk über seinen Anbieter eine gemeinsame Schnittstelle verfügbar macht, kann Windows mit verschiedenen Typen von Netzwerken interagieren, ohne die Netzwerk spezifischen Implementierungsdetails kennen zu müssen.

Der [*multianbieterrouter*](../secgloss/m-gly.md) (MPR) übernimmt die Kommunikation mit allen verschiedenen Netzwerkanbietern im System und stellt dem Benutzer ein integriertes Netzwerk dar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Netzwerkanbieter](network-providers.md)
</dt> <dt>

[Anmeldeinformationsverwaltung](credential-manager.md)
</dt> <dt>

[Mehrere Anbieter Router](multiple-provider-router.md)
</dt> <dt>

[Von Netzwerkanbietern implementierte Funktionen](functions-implemented-by-network-providers.md)
</dt> <dt>

[Credential Management-API](credential-management-api.md)
</dt> <dt>

[Verbindungs Benachrichtigungs-API](connection-notification-api.md)
</dt> </dl>

 

 
