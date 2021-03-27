---
description: Registrierungs Werte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann. Ein Verb erfordert separate Registrierungs Werte für jede dieser drei Situationen, die das Verb unterstützt.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Verwenden des Verb Auswahl Modells
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979576"
---
# <a name="how-to-employ-the-verb-selection-model"></a>Verwenden des Verb Auswahl Modells

Registrierungs Werte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann. Ein Verb erfordert separate Registrierungs Werte für jede dieser drei Situationen, die das Verb unterstützt.

## <a name="instructions"></a>Instructions


Geben Sie den multiselectmodel-Wert für alle Verben an. Wenn der multiselectmodel-Wert nicht angegeben wird, wird er vom Typ der Verb-Implementierung abgeleitet, den Sie ausgewählt haben. Für com- **basierte Methoden (** z. b. "DropTarget" und "ExecuteCommand") wird angenommen, und für die anderen **Methoden wird angenommen** .

Die möglichen Werte für das Verb Auswahl Modell lauten wie folgt:

1.  Geben Sie **Single** für Verben an, die nur eine einzelne Auswahl unterstützen.
2.  Geben Sie **Player** für Verben an, die eine beliebige Anzahl von Elementen unterstützen
3.  Geben Sie ein **Dokument** für Verben an, die für jedes Element ein Fenster auf oberster Ebene erstellen. Dadurch wird die Anzahl der aktivierten Elemente beschränkt, und es wird vermieden, dass Systemressourcen nicht mehr genügend Systemressourcen haben, wenn der Benutzer zu viele Fenster öffnet.

## <a name="remarks"></a>Bemerkungen

Wenn die Anzahl der ausgewählten Elemente nicht mit dem Verb Auswahl Modell identisch ist oder größer als die in der folgenden Tabelle aufgeführten Standard Limits ist, wird das Verb nicht angezeigt.



| Typ der Verb Implementierung | Dokument | Player    |
|-----------------------------|----------|-----------|
| Alt                      | 15 Elemente | 100 Elemente |
| COM                         | 15 Elemente | Keine Begrenzung  |



 

Im folgenden finden Sie Beispiel Registrierungseinträge, die den multiselectmodel-Wert verwenden.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



