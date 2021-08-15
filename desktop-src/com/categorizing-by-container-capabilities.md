---
title: Kategorisieren nach Containerfunktionen
description: Komponenten erfordern häufig bestimmte Funktionen aus dem Container und funktionieren nicht mit einem Container, der die Unterstützung nicht bereitstellt.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67811a40c2c1bbffd4529b3f7c885a0d3e2bea19bda04035ffb80b601c266807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310887"
---
# <a name="categorizing-by-container-capabilities"></a>Kategorisieren nach Containerfunktionen

Komponenten erfordern häufig bestimmte Funktionen aus dem Container und funktionieren nicht mit einem Container, der die Unterstützung nicht bereitstellt. Die Benutzeroberfläche sollte Komponenten herausfiltern, die Funktionen erfordern, die der Container nicht unterstützt. Zu diesem Zweck können Komponenten nach den erforderlichen Containerfunktionen kategorisiert werden.

Ein Beispiel für Komponenten, die Funktionen aus dem Container erfordern und nicht in Containern funktionieren, die diese Funktionalität nicht unterstützen, sind einfache Frame-OLE-Steuerelemente. Die Kategorisierung nach Containerfunktionen erfolgt durch einen zusätzlichen Registrierungsschlüssel im CLSID-Schlüssel der Komponente:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Wie in diesem Beispiel gezeigt, kann eine Komponente zu Komponentenkategorien gehören, die unterstützte Funktionalität angeben, sowie zu Komponentenkategorien, die die erforderliche Funktionalität angeben.

Im folgenden Beispiel ist das Schaltflächensteuerelement ein generisches OLE-Steuerelement, das keine zusätzliche Funktionalität unterstützt. Sie funktioniert in jedem OLE-Steuerelementcontainer.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

Vergleichen Sie das vorherige Beispiel mit dem nächsten Beispiel, in dem MyDBControl Visual Basic Datenbindung verwenden kann, wenn der Container dies unterstützt. Sie wurde jedoch so definiert, dass sie in Containern funktioniert, die Visual Basic Datenbindung (möglicherweise durch eine andere Datenbank-API) nicht unterstützen:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

Das GroupBox-Steuerelement ist ein einfaches Rahmensteuerelement. Er basiert auf dem Container, der die [**ISimpleFrameSite-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) implementiert, und funktioniert nur in solchen Containern ordnungsgemäß:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

Ein Container, der Visual Basic datengebundenen Steuerelementen unterstützt, aber keine einfachen Framesteuerelemente unterstützt, würde CATID \_ Control und CATID \_ VBDatabound für die Benutzeroberfläche des Einfügesteuerelements angeben. Die Liste der Steuerelemente, die dem Benutzer angezeigt werden, würde die \_ CLSID-Schaltfläche und CLSID \_ MyDBControl enthalten. CLSID \_ GroupBox wird nicht angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisieren nach Komponentenfunktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Standardklassen und Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Definieren von Komponentenkategorien](defining-component-categories.md)
</dt> <dt>

[Der Komponentenkategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




