---
title: Der Komponenten Kategorien-Manager
description: Der Komponenten Kategorien-Manager
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471220"
---
# <a name="the-component-categories-manager"></a>Der Komponenten Kategorien-Manager

Um die Verarbeitung von Komponenten Kategorien zu vereinfachen und die Konsistenz der Registrierung zu gewährleisten, stellt das System den Komponenten Kategorien-Manager bereit, ein COM-Objekt mit einer CLSID der CLSID \_ stdcomponentcategoriesmgr. Dieses com-Objekt stellt die folgenden Schnittstellen bereit:

-   [**Ialisierungsinformationen**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**I-Register**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

[**Itorinformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) stellt Methoden zum Abrufen von Informationen über die von einer bestimmten Klasse implementierten oder benötigten Kategorien bereit und stellt Informationen zu den auf einem bestimmten Computer registrierten Kategorien bereit.

[**Ikatregister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) stellt Methoden zum Registrieren und Aufheben der Registrierung von Komponenten Kategorieinformationen in der Registrierung bereit. Dies schließt sowohl die lesbaren Namen von Kategorien als auch die Kategorien ein, die von einer bestimmten Komponente oder Klasse implementiert oder benötigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisierung nach Komponenten Funktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Kategorisierung nach Container Funktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Standardklassen und-Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Definieren von Komponenten Kategorien](defining-component-categories.md)
</dt> </dl>

 

 




