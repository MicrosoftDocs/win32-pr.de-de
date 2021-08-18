---
title: Dynamisch verknüpfte Hilfsklassen
description: Eine dynamisch verknüpfte Hilfsklasse ist eine Klasse, die an ein einzelnes Objekt und nicht an eine Objektklasse angefügt ist.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Dynamisch verknüpfte Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5fc73ef64e1ed4af0dd73879dc1cd7ed8b2d82ac1d397db001c1487680b13b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695373"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Dynamisch verknüpfte Hilfsklassen

Eine dynamisch verknüpfte Hilfsklasse ist eine Klasse, die an ein einzelnes Objekt und nicht an eine Objektklasse angefügt ist. Mit der dynamischen Verknüpfung können Sie zusätzliche Attribute mit einem einzelnen Objekt speichern, ohne die gesamtstrukturweite Auswirkung der Erweiterung der Schemadefinition für eine gesamte Klasse zu haben. Ein Unternehmen könnte z. B. dynamische Verknüpfungen verwenden, um eine vertriebsspezifische Hilfsklasse an die Benutzerobjekte seiner Vertriebsmitarbeiter und andere abteilungsspezifische Hilfsklassen an die Benutzerobjekte von Mitarbeitern in anderen Abteilungen anfügen.

Dynamisches Verknüpfen ist nicht komplex: Fügen Sie den Namen der Hilfsklasse den Werten des **objectClass-Attributs eines Objekts** hinzu. Wenn die Hilfsklasse über obligatorische Attribute verfügt (**mustHave** oder **systemMustHave**), müssen Sie sie gleichzeitig festlegen. Weitere Informationen und ein Codebeispiel finden Sie unter [Adding an Auxiliary Class to an Object Instance](adding-an-auxiliary-class-to-an-object-instance.md).

Um eine dynamisch verknüpfte Hilfsklasse zu entfernen, löschen Sie die Werte aller Attribute aus der Hilfsklasse, und entfernen Sie dann den Namen der Hilfsklasse aus dem **objectClass-Attribut** des -Objekts.

Wenn Sie dynamisch eine Hilfsklasse hinzufügen, die eine Unterklasse einer anderen Hilfsklasse ist, werden beide Hilfsklassen dem Zielobjekt hinzugefügt. Durch das Entfernen der untergeordneten Hilfsklasse wird das übergeordnete Element jedoch nicht entfernt. jede Klasse muss explizit entfernt werden.

 

 




