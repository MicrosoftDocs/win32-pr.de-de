---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Abbildverwaltung für die Bereitstellung (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369856"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Abbildverwaltung für die Bereitstellung (DISM)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows Vista SP1 und höher \| Windows 7  
**Server** -Windows Server 2008 RTM und höher \| Windows Server 2008 R2  


## <a name="description"></a>BESCHREIBUNG

Das Tool zur Abbild Verwaltung für die Bereitstellung (Mage) ersetzt die Tools pkgmgr, peimg und intlconfg, die in Windows 7 eingestellt werden. Das-Verfahren bietet ein zentrales Tool für die Durchführung aller Funktionen dieser drei Tools auf effizientere und standardisierte Weise. Dadurch entfällt die Quelle vieler der Frustrationen, die von den aktuellen Benutzern dieser Tools genutzt werden.

Der-Wert enthält einen Shim für Windows Vista SP1 und höher sowie für Windows Server 2008 RTM und höher, der pkgmgr-Aufrufe von älteren Anwendungen unter Windows 7 an den-Dienst umleitet. Wenn die Anwendung unter einem der unterstützten Betriebssysteme ausgeführt wird, leitet der Shim den pkgmgr-Rückruf. Für Legacy Anwendungen, die peimg oder intlconfg anrufen, sind keine Shims vorhanden.

## <a name="usage"></a>Verbrauch

Das-Paradigma ist für pkgmgr-Endbenutzer auf allen unterstützten Plattformen transparent. Wenn eine Anwendung jedoch entweder peimg oder intlconfg von Windows 7 aufruft, schlägt der Aufruf fehl.

Aktualisieren Sie alle Skripts, die pkgmgr, peimg oder intlconfg anrufen, um stattdessen die-Funktion aufzurufen. Es ist wichtig, dass Sie die Aktualisierung von Pkgmgr-Skripts in diesen Vorgang einschließen, da das Shim, das Abwärtskompatibilität für pkgmgr bereitstellt, in zukünftigen Versionen der Windows-Betriebssysteme entfernt wird.

Stellen Sie sicher, dass Aufrufe der-Funktion alle Aufrufe von Pkgmgr, peimg und intlconfg ersetzt haben und der Vorgang erfolgreich ausgeführt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Abbild Verwaltung für die Bereitstellung (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
