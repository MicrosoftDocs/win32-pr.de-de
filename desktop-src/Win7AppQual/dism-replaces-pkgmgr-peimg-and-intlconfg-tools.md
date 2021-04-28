---
description: Abbildverwaltung für die Bereitstellung (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Abbildverwaltung für die Bereitstellung (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088488"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Abbildverwaltung für die Bereitstellung (DISM)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** : Windows Vista SP1 und höher \| Windows 7  
**Server** : Windows Server 2008 RTM und höher \| Windows Server 2008 R2  


## <a name="description"></a>BESCHREIBUNG

Das dism-Tool (Abbildverwaltung für die Bereitstellung) ersetzt die Tools pkgmgr, PEImg und IntlConfg, die in Windows 7 eingestellt werden. DISM bietet ein einzelnes zentralisiertes Tool, mit dem alle Funktionen dieser drei Tools effizienter und standardisierter ausgeführt werden können, sodass viele der frustrierten Benutzer dieser Tools nicht mehr auftreten können.

DISM enthält einen Shim für Windows Vista SP1 und höher sowie für Windows Server 2008 RTM und höher, der pkgmgr-Aufrufe von Legacyanwendungen, die unter Windows 7 ausgeführt werden, an DISM umleitet. Wenn die Anwendung unter einem der unterstützten Betriebssysteme ausgeführt wird, leitet der Shim den Aufruf an pkgmgr weiter. Für Legacyanwendungen, die PEImg oder IntlConfg aufrufen, sind keine Shims vorhanden.

## <a name="usage"></a>Verbrauch

DISM ist für pkgmgr-Endbenutzer auf allen unterstützten Plattformen transparent. Wenn eine Anwendung jedoch entweder PEImg oder IntlConfg von Windows 7 aufruft, schlägt der Aufruf fehl.

Aktualisieren Sie alle Skripts, die pkgmgr, PEImg oder IntlConfg aufrufen, um stattdessen DISM aufzurufen. Es ist wichtig, die Aktualisierung von pkgmgr-Skripts in diesen Aufwand einzubeziehen, da der Shim, der Abwärtskompatibilität für pkgmgr bereitstellt, in zukünftigen Versionen der Windows-Betriebssysteme entfernt wird.

Überprüfen Sie, ob Aufrufe von DISM alle Aufrufe von pkgmgr, PEImg und IntlConfg ersetzt haben und dass der Vorgang erfolgreich ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abbildverwaltung für die Bereitstellung (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
