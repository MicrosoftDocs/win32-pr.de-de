---
description: Abbildverwaltung für die Bereitstellung (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Abbildverwaltung für die Bereitstellung (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6da1cc8ec3e77a6c63df8e44917cb5f3474ae8e7a5e34b58f49255fa34b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053178"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Abbildverwaltung für die Bereitstellung (DISM)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows Vista SP1 und \| höher Windows 7  
**Server** – Windows Server 2008 RTM \| und höher Windows Server 2008 R2  


## <a name="description"></a>Beschreibung

Das Abbildverwaltung für die Bereitstellung -Tool (DISM) ersetzt die Tools pkgmgr, PEImg und IntlConfg, die in Windows 7 eingestellt werden. DISM bietet ein zentrales Tool, um alle Funktionen dieser drei Tools effizienter und standardisierter auszuführen, wodurch viele der Frusts der aktuellen Benutzer dieser Tools beseitigt werden.

DISM enthält einen Shim für Windows Vista SP1 und höher sowie für Windows Server 2008 RTM und höher, der pkgmgr-Aufrufe von Legacyanwendungen, die unter Windows 7 ausgeführt werden, an DISM umleiten. Wenn die Anwendung unter einem der unterstützten Betriebssysteme ausgeführt wird, leitet der Shim den Aufruf an pkgmgr weiter. Für Legacyanwendungen, die PEImg oder IntlConfg aufrufen, sind keine Shims vorhanden.

## <a name="usage"></a>Verwendung

DISM ist für pkgmgr-Endbenutzer auf einer der unterstützten Plattformen transparent. Wenn eine Anwendung jedoch entweder PEImg oder IntlConfg aus Windows 7 aufruft, wird der Aufruf fehlschlagen.

Aktualisieren Sie alle Skripts, die pkgmgr, PEImg oder IntlConfg aufrufen, um stattdessen DISM aufrufen. Es ist wichtig, die Aktualisierung von pkgmgr-Skripts in diesen Aufwand zu integrieren, da der Shim, der Abwärtskompatibilität für pkgmgr bietet, in zukünftigen Versionen des Windows entfernt wird.

Stellen Sie sicher, dass Aufrufe von DISM alle Aufrufe von pkgmgr, PEImg und IntlConfg ersetzt haben und dass der Vorgang erfolgreich ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abbildverwaltung für die Bereitstellung (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
