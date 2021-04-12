---
title: Dynamisch verknüpfte Hilfsklassen
description: Eine dynamisch verknüpfte Hilfsklasse ist eine Klasse, die an ein einzelnes Objekt angefügt ist, und nicht an eine Objektklasse.
ms.assetid: 10530a3c-89fc-4ff0-a0b7-1c9a27659003
ms.tgt_platform: multiple
keywords:
- Dynamisch verknüpfte Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0cacb09d3aef05bcaf0ef729411c2e023469be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206275"
---
# <a name="dynamically-linked-auxiliary-classes"></a>Dynamisch verknüpfte Hilfsklassen

Eine dynamisch verknüpfte Hilfsklasse ist eine Klasse, die an ein einzelnes Objekt angefügt ist, und nicht an eine Objektklasse. Mithilfe dynamischer Verknüpfungen können Sie zusätzliche Attribute mit einem einzelnen Objekt speichern, ohne die Gesamtstruktur weite Auswirkung der Erweiterung der Schema Definition für eine ganze Klasse zu haben. Beispielsweise könnte ein Unternehmen mithilfe dynamischer Verknüpfungen eine Verkaufs spezifische Hilfsklasse an die Benutzer Objekte seiner Vertriebsmitarbeiter und andere abteilungsspezifische Hilfssysteme an die Benutzer Objekte der Mitarbeiter in anderen Abteilungen anfügen.

Dynamisches Verknüpfen ist nicht komplex: Fügen Sie den Werten eines **objectClass** -Attributs für ein Objekt den Namen der Hilfsklasse hinzu. Wenn die Erweiterungs Klasse über obligatorische Attribute (**musthave** oder **systemmusthave**) verfügt, müssen Sie Sie gleichzeitig festlegen. Weitere Informationen und ein Codebeispiel finden Sie unter [Hinzufügen einer zusätzlichen Klasse zu einer Objektinstanz](adding-an-auxiliary-class-to-an-object-instance.md).

Um eine dynamisch verknüpfte Hilfsklasse zu entfernen, löschen Sie die Werte aller Attribute aus der Erweiterungs Klasse, und entfernen Sie dann den Namen der Hilfsklasse aus dem **objectClass** -Attribut des Objekts.

Wenn Sie eine zusätzliche Klasse dynamisch hinzufügen, die eine Unterklasse einer anderen Hilfsklasse ist, werden dem Zielobjekt beide Erweiterungs Klassen hinzugefügt. Das Entfernen der untergeordneten Erweiterungs Klasse entfernt jedoch nicht das übergeordnete Element. jede Klasse muss explizit entfernt werden.

 

 




