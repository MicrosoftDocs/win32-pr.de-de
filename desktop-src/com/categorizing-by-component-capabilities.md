---
title: Kategorisierung nach Komponenten Funktionen
description: Komponenten Kategorien können verwendet werden, um eine Teilmenge aller installierten Komponenten anzuzeigen.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff44e03e9eae0226ac57279c37d4a5dfd32fc6bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341434"
---
# <a name="categorizing-by-component-capabilities"></a>Kategorisierung nach Komponenten Funktionen

Komponenten Kategorien können verwendet werden, um eine Teilmenge aller installierten Komponenten anzuzeigen. Jede Komponenten Kategorie wird durch eine GUID identifiziert, die als Kategorie-ID (CATID) bezeichnet wird. Jede CATID verfügt über eine Liste von mit dem Gebiets Schema markierten, lesbaren Namen. Eine Auflistung der CATIDs und der lesbaren Namen wird an einem bekannten Speicherort in der Registrierung gespeichert.

Beispielsweise können alle Komponenten, die die Funktionalität für die Einbettung von OLE-Dokumenten implementieren, in einer Komponenten Kategorie klassifiziert werden. In der Vergangenheit wurden diese Objekte durch den Schlüssel "Insertable" in der Registrierung identifiziert. Um stattdessen Komponenten Kategorien zu verwenden, werden der Registrierung die folgenden Informationen hinzugefügt:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Jede Klasse, die die Funktionalität implementiert, die einer Komponenten Kategorie entspricht, listet die Kategorie-ID für diese Kategorie innerhalb des CLSID-Schlüssels in der Registrierung auf. Da eine einzelne Komponente eine große Bandbreite von Funktionen unterstützen kann, können Komponenten mehreren Komponenten Kategorien angehören. Beispielsweise kann ein bestimmtes OLE-Steuerelement sämtliche Funktionen unterstützen, die für die Teilnahme als OLE-Dokument Einbettung, Microsoft Visual Basic-Datenbindung und Internet Funktionalität erforderlich sind. Für ein solches Steuerelement sind die folgenden Informationen im CLSID-Schlüssel in der Registrierung gespeichert:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Mit diesen Informationen kann ein Container die auf einem System installierten Steuerelemente auflisten und nur die Steuerelemente anzeigen, die die für den Container erforderliche Funktionalität unterstützen. Die Verwendung von Komponenten Kategorien bietet eine Möglichkeit, Komponenten nach den implementierten Funktionen der Komponente zu kategorisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisierung nach Container Funktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Standardklassen und-Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Definieren von Komponenten Kategorien](defining-component-categories.md)
</dt> <dt>

[Der Komponenten Kategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




