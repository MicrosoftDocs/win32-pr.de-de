---
title: Zuordnen von Symbolen zu einer Kategorie
description: Zuordnen von Symbolen zu einer Kategorie
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036489"
---
# <a name="associating-icons-with-a-category"></a>Zuordnen von Symbolen zu einer Kategorie

Das Entwickeln einer Benutzeroberfläche, die es dem Benutzer ermöglicht, Komponenten Kategorien innerhalb einer Kategorie auszuwählen, erfordert die Möglichkeit, ein aussagekräftiges Bild für eine bestimmte Kategorie anzuzeigen. Wenn Sie ein Symbol einer Komponenten Kategorie zuordnen möchten, erstellen Sie einen Schlüssel für die CATID der Kategorie, und füllen Sie den Schlüssel mit einem [DefaultIcon](defaulticon.md) -Unterschlüssel auf. Der Registrierungs Eintrag lautet wie folgt:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

Der Dateiname, auf den der DefaultIcon-Schlüssel verweist, kann entweder eine exe-oder DLL-Datei (reine Ressourcen-DLL) sein.

Um einer Komponenten Kategorie eine kleine 16x16-"Toolbox Bitmap" zuzuordnen, erstellen Sie einen Schlüssel in der **HKEY-Klassen Stamm- \_ \_ \\ CLSID** für die CATID der Kategorie und füllen den Schlüssel mit einem [ToolBoxBitmap32](toolboxbitmap32.md) -Unterschlüssel auf, wie im folgenden Beispiel gezeigt:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

Der Dateiname, auf den der [ToolBoxBitmap32](toolboxbitmap32.md) -Schlüssel verweist, kann auch eine exe-oder DLL-Datei (reine Ressourcen-DLL) sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kategorisierung nach Komponenten Funktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Kategorisierung nach Container Funktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Standardklassen und-Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Definieren von Komponenten Kategorien](defining-component-categories.md)
</dt> <dt>

[**Ialisierungsinformationen**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**I-Register**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[Der Komponenten Kategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




