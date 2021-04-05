---
title: Kategorisierung nach Container Funktionen
description: Komponenten erfordern häufig bestimmte Funktionen aus dem Container und funktionieren nicht mit einem Container, der keine Unterstützung bietet.
ms.assetid: 11002f3e-17de-4e05-a2df-0c9e6326846d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987546c20ff77a40666bb74689466a15fab989a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037530"
---
# <a name="categorizing-by-container-capabilities"></a>Kategorisierung nach Container Funktionen

Komponenten erfordern häufig bestimmte Funktionen aus dem Container und funktionieren nicht mit einem Container, der keine Unterstützung bietet. Die Benutzeroberfläche sollte Komponenten herausfiltern, die Funktionen erfordern, die der Container nicht unterstützt. Um dies zu erreichen, können Komponenten nach den erforderlichen Container Funktionen kategorisiert werden.

Ein Beispiel für Komponenten, die Funktionen aus dem Container erfordern und nicht in Containern funktionieren, die diese Funktionalität nicht unterstützen, sind einfache Frame-OLE-Steuerelemente. Die Kategorisierung nach Container Funktionen erfolgt durch einen zusätzlichen Registrierungsschlüssel innerhalb des CLSID-Schlüssels der Komponente:

``` syntax
;The CLSID for "Simple Frame Control" is {123456FF-ABCD-4321-0101-00000000000C}HKEY_CASSES_ROOT\CLSID\{12346FF-ABCD-4321-0101-00000000000C}\Implemented Categories
;The CATID for "Control" is {40FC6ED4-2438-11cf-A3DB-080036F12502} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{40FC6ED4-2438-11cf-A3DB-080036F12502}
;The CATID for simple frame controls is {...CATID_SimpleFrameControl...} HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Implemented Categories\{...CATID_SimpleFrameControl...}
HKEY_CLASSES_ROOT\CLSID\{123456FF-ABCD-4321-0101-00000000000C}Required Categories\{...CATID_SimpleFrameControl...}
 
```

Wie in diesem Beispiel gezeigt, kann eine Komponente zu Komponenten Kategorien gehören, die auf unterstützte Funktionen hinweisen, sowie auf Komponenten Kategorien, die die erforderliche Funktionalität angeben.

Im folgenden Beispiel ist das Schaltflächen-Steuerelement ein generisches OLE-Steuerelement, das keine zusätzliche Funktionalität unterstützt. Es funktioniert in jedem OLE-Steuerelement Container.

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_Button...}\Implemented Categories\{...CATID_Control...}
 
```

Vergleichen Sie das vorangehende Beispiel mit dem nächsten Beispiel, in dem mydbcontrol Visual Basic Datenbindung verwenden kann, wenn es vom Container unterstützt wird. Sie wurde jedoch so definiert, dass Sie in Containern funktioniert, die keine Visual Basic Datenbindung unterstützen (möglicherweise durch eine andere Datenbank-API):

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_MyDBControl...}\Implemented Categories\{...CATID_VBDatabound...}
 
```

Das GroupBox-Steuerelement ist ein einfaches Frame-Steuerelement. Er basiert auf dem Container, der die [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) -Schnittstelle implementiert, und funktioniert nur in solchen Containern ordnungsgemäß:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_Control...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Implemented Categories\{...CATID_SimpleFrame...}
HKEY_CLASSES_ROOT\CLSID\{...CLSID_GroupBox...}\Required Categories\{...CATID_SimpleFrame...}
 
```

Ein Container, der Visual Basic Daten gebundene Steuerelemente unterstützt, aber keine einfachen Frame Steuerelemente unterstützt, würde das CATID- \_ Steuerelement und CATID \_ vbdatbound an die Benutzeroberfläche des einfügesteuerelements Die Liste der Steuerelemente, die dem Benutzer angezeigt werden, enthält die CLSID \_ -Schaltfläche und die CLSID \_ mydbcontrol. Die CLSID- \_ GroupBox wird nicht angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisierung nach Komponenten Funktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Standardklassen und-Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Definieren von Komponenten Kategorien](defining-component-categories.md)
</dt> <dt>

[Der Komponenten Kategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




