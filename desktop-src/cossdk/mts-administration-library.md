---
description: Die im Lieferumfang der COM+-Verwaltungsschnittstellen enthaltene MTS-Verwaltungsbibliothek bietet Abwärtskompatibilität mit der MTS 2.0-Verwaltungsbibliothek.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: MTS-Verwaltungsbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e449e99ef675f7f8ce893a358806926cd3d1a63ed13e5cc9fff01b97d0742d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306158"
---
# <a name="mts-administration-library"></a>MTS-Verwaltungsbibliothek

Die im Lieferumfang der COM+-Verwaltungsschnittstellen enthaltene MTS-Verwaltungsbibliothek bietet Abwärtskompatibilität mit der MTS 2.0-Verwaltungsbibliothek. Die meisten vorhandenen MTS 2.0-Verwaltungscodes funktionieren weiterhin mit der bereitgestellten MTSAdmin-Bibliothek. einige Funktionen wurden jedoch geändert.

Wenn Sie neue Funktionen nutzen oder verwaltungscode zum ersten Mal schreiben möchten, sollten Sie die COMAdmin-Bibliothek verwenden.

Die folgenden Elemente in der aktuellen MTS-Verwaltungsbibliothek werden von der MTS 2.0-Verwaltungsbibliothek geändert:

-   Die **IRemoteComponentUtil-Schnittstelle** ist nicht mehr verfügbar.
-   Die **RemoteComponents-Auflistung** ist nicht mehr verfügbar.
-   Die RoleID-Eigenschaft ist nicht mehr verfügbar. Der Rollenname wird jetzt als Schlüssel dafür verwendet.
-   Die **ExportPackage-Methode** exportiert keine client.exe mehr.
-   Die RemoteComponentInstallPath-Eigenschaft wird nicht mehr für die [**LocalComputer-Auflistung**](localcomputer.md) verfügbar gemacht.
-   Die ApplicationInstallPath-Eigenschaft wird nicht mehr für die [**LocalComputer-Sammlung**](localcomputer.md) verfügbar gemacht.
-   Das Systempaket heißt jetzt Systemanwendung.
-   Das Hilfsprogrammpaket heißt jetzt COM+-Hilfsprogramme.
-   Die IsSystem-Eigenschaft ist in der [**Components-Auflistung**](components.md) in MTSAdmin vorhanden, gibt jedoch bei Aktiviert "NotImpl" zurück und wird nicht gespeichert, wenn festgelegt.
-   Die PackageName-Eigenschaft wird von der [**Components-Auflistung**](components.md) nicht mehr unterstützt. Um den Namen des Pakets zu ermitteln, müssen Sie jetzt die PackageID abrufen und dann das übereinstimmende Paket in der Packages-Sammlung suchen.
-   Die folgenden Eigenschaften sind in der [**InterfacesForComponent-Auflistung**](interfacesforcomponent.md) nicht mehr vorhanden:
    -   **ProxyCLSID**
    -   **ProxyDLL**
    -   **ProxyThreadingModel**
    -   **TypeLibFile**
    -   **TypeLibID**
    -   **TypeLibLangID**
    -   **TypeLibPlatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Automatische Konvertierung von MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[COM+-Konvertierungsergebnisse und -Probleme](com--conversion-results-and-issues.md)
</dt> <dt>

[Manuelle Konvertierung von MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



