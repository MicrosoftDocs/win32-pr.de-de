---
title: Kategorisieren nach Komponentenfunktionen
description: Komponentenkategorien können verwendet werden, um eine Teilmenge aller installierten Komponenten anzuzeigen.
ms.assetid: 522af5d7-ba7b-4127-9cdb-48ef4d0f8e65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 251e8197c00a39c8d9666dee7122be7445402fc84ce7b3508987bcf79f27df15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048748"
---
# <a name="categorizing-by-component-capabilities"></a>Kategorisieren nach Komponentenfunktionen

Komponentenkategorien können verwendet werden, um eine Teilmenge aller installierten Komponenten anzuzeigen. Jede Komponentenkategorie wird durch eine GUID identifiziert, die als Kategorie-ID (CATID) bezeichnet wird. Jeder CATID ist eine Liste mit durch das Locale markierten, für Menschen lesbaren Namen zugeordnet. Eine Liste der CATIDs und der für Menschen lesbaren Namen wird an einem bekannten Speicherort in der Registrierung gespeichert.

Beispielsweise können alle Komponenten, die die Funktionalität für das Einbetten von OLE-Dokumenten implementieren, innerhalb einer Komponentenkategorie klassifiziert werden. In der Vergangenheit wurden diese Objekte durch den Schlüssel "Insertable" in der Registrierung identifiziert. Um stattdessen Komponentenkategorien zu verwenden, werden der Registrierung die folgenden Informationen hinzugefügt:

```
HKEY_CLASSES_ROOT\Component Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
   (Default) = ""
   409 = "Embeddable Objects"
```

Jede Klasse, die die einer Komponentenkategorie entsprechende Funktionalität implementiert, listet die Kategorie-ID für diese Kategorie innerhalb des CLSID-Schlüssels in der Registrierung auf. Da eine einzelne Komponente eine Vielzahl von Funktionen unterstützen kann, können Komponenten zu mehreren Komponentenkategorien gehören. Beispielsweise kann ein bestimmtes OLE-Steuerelement alle Funktionen unterstützen, die erforderlich sind, um als OLE-Dokument-Einbettung, Microsoft Visual Basic-Datenbindung und Internetfunktionalität teilzunehmen. Bei einem solchen Steuerelement werden die folgenden Informationen im CLSID-Schlüssel in der Registrierung gespeichert:

``` syntax
;The CLSID for "My Super OLE Control" is {12345678-ABCD-4321-0101-00000000000C}HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Insertable" is {40FC6ED3-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED3-2438-11cf-A3DB-080036F12502}
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for an internet aware control is {...CATID_InternetAware...} HKEY_CLASSES_ROOT\CLSID\{12345678-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_InternetAware...}
 
```

Mit diesen Informationen kann ein Container die auf einem System installierten Steuerelemente aufzählen und nur die Steuerelemente anzeigen, die die für den Container erforderliche Funktionalität unterstützen. Die Verwendung von Komponentenkategorien bietet eine Möglichkeit, Komponenten nach der implementierten Funktionalität der Komponente zu kategorisieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisieren nach Containerfunktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Standardklassen und Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Definieren von Komponentenkategorien](defining-component-categories.md)
</dt> <dt>

[Der Komponentenkategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




