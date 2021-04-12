---
title: Standardklassen und-Zuordnungen
description: Für bestimmte Kategorien kann eine einzelne Klasse als Standardklasse zugeordnet werden.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387981"
---
# <a name="default-classes-and-associations"></a>Standardklassen und-Zuordnungen

Für bestimmte Kategorien kann eine einzelne Klasse als Standardklasse zugeordnet werden. Die Standardklasse wird immer dann ausgewählt, wenn eine bestimmte Objekt Kategorie erforderlich ist. Obwohl dies für alle Komponenten Kategorien nicht nützlich sein kann, kann das Einrichten einer Standardklasse hilfreich sein, wenn eine bestimmte Klasse aus einer Liste möglicher Klassen geladen werden muss, ohne dass ein Benutzereingriff erforderlich ist. Administratoren definieren, welche Klasse durch die Bearbeitung der Registrierung verwendet werden kann.

Um einer Kategorie eine Standardklasse zuzuordnen, führen Sie einen CLSID-Schlüssel mit der gleichen CLSID wie die CATID der als Standard ausgewählten Komponenten Kategorie ein. Fügen Sie diesem Schlüssel dann einen TreatAs-Schlüssel mit dem Wert für die CLSID der Standardklasse für die Kategorie hinzu. Um die Standardklasse für eine Komponenten Kategorie zu verwenden, verwenden Sie [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), wobei Sie die CATID für den CLSID-Parameter angeben. Dadurch wird automatisch zur CLSID umgeleitet, die als Standard für diese Kategorie festgelegt wurde. Der Registrierungs Eintrag lautet wie folgt:

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

Während der Installation kann eine Komponente überprüfen, ob alle Standardklassen Schlüssel für Ihre Kategorien vorhanden sind, und den Benutzern Optionen zum Überschreiben der aktuellen Einstellungen präsentieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zuordnen von Symbolen zu einer Kategorie](associating-icons-with-a-category.md)
</dt> <dt>

[Kategorisierung nach Komponenten Funktionen](categorizing-by-component-capabilities.md)
</dt> <dt>

[Kategorisierung nach Container Funktionen](categorizing-by-container-capabilities.md)
</dt> <dt>

[Definieren von Komponenten Kategorien](defining-component-categories.md)
</dt> <dt>

[Der Komponenten Kategorien-Manager](the-component-categories-manager.md)
</dt> </dl>

 

 




