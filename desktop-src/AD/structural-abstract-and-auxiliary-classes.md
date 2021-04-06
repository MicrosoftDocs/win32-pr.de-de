---
title: Struktur-, abstrakte und Hilfsklassen
description: Das objectClassCategory-Attribut eines classSchema-Objekts kann über einen Wert verfügen, der in der folgenden Tabelle aufgeführt ist und angibt, ob die Klasse strukturell, abstrakt oder hilfsweise ist.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Struktur-, abstrakte und Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561bc836794b45b6c028fe8da772b0b38d0936a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036338"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>Struktur-, abstrakte und Hilfsklassen

Das **objectClassCategory** -Attribut eines **classSchema** -Objekts kann über einen Wert verfügen, der in der folgenden Tabelle aufgeführt ist und angibt, ob die Klasse strukturell, abstrakt oder hilfsweise ist.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Eine strukturelle Klasse, bei der es sich um den einzigen Typ der Klasse handelt, die über Instanzen in Active Directory Domain Services verfügen kann. Eine strukturelle Klasse kann eine Unterklasse einer abstrakten oder strukturellen Klasse sein. Eine strukturelle Klasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten.                                                                                                                                                                                                                                           |
| 2     | Eine abstrakte Klasse, bei der es sich um eine Vorlage handelt, mit der neue abstrakte, zusätzliche und strukturelle Klassen abgeleitet werden. Eine abstrakte Klasse kann nur eine Unterklasse einer abstrakten Klasse sein. Abstrakte Klassen können nicht in Active Directory Domain Services instanziiert werden. Eine abstrakte Klasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten.                                                                                                                                                                                   |
| 3     | Eine Hilfsklasse, die in die Definition einer Struktur-, abstrakten oder Erweiterungs Klasse eingeschlossen werden kann. in diesem Fall werden die Werte **mustare**, **systemmustare**, **mayare** und **systemmayare** der Erweiterungs Klasse den Werten der Klasse hinzugefügt. Eine Hilfsklasse kann eine Unterklasse einer abstrakten oder einer Hilfsklasse sein. Erweiterungs Klassen können nicht in Active Directory Domain Services instanziiert werden. Eine Hilfsklasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten. |



 

Verwechseln Sie **objectClassCategory** nicht mit einer [Objekt Kategorie](object-class-and-object-category.md).

 

 




