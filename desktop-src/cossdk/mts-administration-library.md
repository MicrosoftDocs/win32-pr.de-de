---
description: Die in den com+-Verwaltungs Schnittstellen enthaltene MTS-Verwaltungs Bibliothek bietet Abwärtskompatibilität mit der MTS 2,0-Verwaltungs Bibliothek.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: MTS-Verwaltungs Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523539"
---
# <a name="mts-administration-library"></a>MTS-Verwaltungs Bibliothek

Die in den com+-Verwaltungs Schnittstellen enthaltene MTS-Verwaltungs Bibliothek bietet Abwärtskompatibilität mit der MTS 2,0-Verwaltungs Bibliothek. Der größte vorhandene MTS 2,0-Verwaltungs Code funktioniert weiterhin mit der bereitgestellten msadmin-Bibliothek. Allerdings haben sich einige Funktionen geändert.

Um die neuen Funktionen nutzen zu können, oder wenn Sie zum ersten Mal Verwaltungs Code schreiben, sollten Sie die COMAdmin-Bibliothek verwenden.

Die folgenden Elemente in der aktuellen MTS-Verwaltungs Bibliothek werden in der Bibliothek "MTS 2,0-Verwaltung" geändert:

-   Die **iremotecomponentutil** -Schnittstelle ist nicht mehr verfügbar.
-   Die **RemoteComponents** -Sammlung ist nicht mehr verfügbar.
-   Die RoleID-Eigenschaft ist nicht mehr verfügbar. der Rollen Name wird jetzt als Schlüssel für dieses verwendet.
-   Die **exportpackage** -Methode exportiert keine client.exe mehr.
-   Die remotecomponentinstallpath-Eigenschaft wird nicht mehr in der [**LocalComputer**](localcomputer.md) -Sammlung verfügbar gemacht.
-   Die applicationinstallpath-Eigenschaft wird nicht mehr in der [**LocalComputer**](localcomputer.md) -Sammlung verfügbar gemacht.
-   Das System Paket heißt jetzt Systemanwendung.
-   Das Hilfsprogrammpaket heißt jetzt com+-Hilfsprogramme.
-   Die IsSystem-Eigenschaft ist in der [**Components**](components.md) -Auflistung in mtadmin vorhanden, gibt jedoch "notimpl" zurück, wenn Sie aktiviert ist, und wird nicht gespeichert, wenn Sie festgelegt ist.
-   Die PackageName-Eigenschaft wird von der [**Components**](components.md) -Auflistung nicht mehr unterstützt. Zum Ermitteln des Paket namens müssen Sie nun die PackageID abrufen und dann das entsprechende Paket in der Paket Auflistung suchen.
-   Die folgenden Eigenschaften sind in der [**interfakesforcomponent**](interfacesforcomponent.md) -Sammlung nicht mehr vorhanden:
    -   **Proxyclsid**
    -   **Proxydll**
    -   **Proxythreadingmodel**
    -   **TypeLibFile**
    -   **TypeLibID**
    -   **Typeliblangid**
    -   **Typelibplatform**
    -   **TypeLibVersion**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Automatische Konvertierung von MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Ergebnisse und Probleme bei der com+-Konvertierung](com--conversion-results-and-issues.md)
</dt> <dt>

[Manuelle Konvertierung von MTS](manual-conversion-from-mts.md)
</dt> </dl>

 

 



