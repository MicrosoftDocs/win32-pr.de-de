---
title: Zuordnen von Symbolen zu einer Kategorie
description: Zuordnen von Symbolen zu einer Kategorie
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62af14480d24053ffc517d405635ecbe4d6e45c8edac256039ea008160f11063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793830"
---
# <a name="associating-icons-with-a-category"></a>Zuordnen von Symbolen zu einer Kategorie

Das Erstellen einer Benutzeroberfläche, die es dem Benutzer ermöglicht, Komponentenkategorien innerhalb einer Kategorie auszuwählen, erfordert die Möglichkeit, ein aussagekräftiges Bild für eine bestimmte Kategorie anzuzeigen. Um ein Symbol einer Komponentenkategorie zuzuordnen, erstellen Sie einen Schlüssel für die CATID der Kategorie, und füllen Sie diesen Schlüssel mit einem [DefaultIcon-Unterschlüssel](defaulticon.md) auf. Der Registrierungseintrag lautet wie folgt:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

Der Dateiname, auf den der DefaultIcon-Schlüssel verweist, kann entweder eine EXE- oder eine DLL-Datei (rein ressourcenbezogene DLL) sein.

Um eine kleine 16x16-Toolboxbitmap einer Komponentenkategorie zuzuordnen, erstellen Sie einen Schlüssel in **HKEY \_ CLASSES ROOT \_ \\ CLSID** für die CATID der Kategorie und füllen diesen Schlüssel mit einem [ToolBoxBitmap32-Unterschlüssel](toolboxbitmap32.md) auf, wie im folgenden Beispiel gezeigt:

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

Der Dateiname, auf den der [ToolBoxBitmap32-Schlüssel](toolboxbitmap32.md) verweist, kann auch eine EXE- oder DLL-Datei (nur ressourcenbasierte DLL) sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kategorisieren nach Komponentenfunktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Kategorisieren nach Containerfunktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Standardklassen und Zuordnungen](default-classes-and-associations.md)
</dt> <dt>

[Definieren von Komponentenkategorien](defining-component-categories.md)
</dt> <dt>

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[Komponentenkategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




