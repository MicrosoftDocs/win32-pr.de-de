---
title: Strukturelle, abstrakte und Hilfsklassen
description: Das objectClassCategory-Attribut eines classSchema-Objekts kann über einen Wert verfügen, wie in der folgenden Tabelle aufgeführt, der angibt, ob die Klasse strukturell, abstrakt oder hilfsklassig ist.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Strukturelle, abstrakte und Hilfsklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393c08f5c26690d5b08b76dfea8ab4ff2833c94851a10ddcea2a69209279fbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024708"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>Strukturelle, abstrakte und Hilfsklassen

Das **objectClassCategory-Attribut** eines **classSchema-Objekts** kann über einen Wert verfügen, wie in der folgenden Tabelle aufgeführt, der angibt, ob die Klasse strukturell, abstrakt oder hilfsklassig ist.



| Wert | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Eine strukturelle Klasse, bei der es sich um den einzigen Klassentyp handelt, der Überinstanzen in der Active Directory Domain Services. Eine strukturelle Klasse kann eine Unterklasse einer abstrakten oder strukturellen Klasse sein. Eine strukturelle Klasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten.                                                                                                                                                                                                                                           |
| 2     | Eine abstrakte Klasse, bei der es sich um eine Vorlage handelt, die zum Ableiten neuer abstrakter, hilfsiver und struktureller Klassen verwendet wird. Eine abstrakte Klasse kann nur eine Unterklasse einer abstrakten Klasse sein. Abstrakte Klassen können in der -Klasse nicht instanziiert Active Directory Domain Services. Eine abstrakte Klasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten.                                                                                                                                                                                   |
| 3     | Eine Hilfsklasse, die in die Definition einer strukturellen, abstrakten oder Hilfsklasse eingeschlossen werden kann. In diesem Fall werden die **mustContain-,** **systemMustContain-,** **mayContain-** und **systemMayContain-Werte** der Hilfsklasse den Werten der -Klasse hinzugefügt. Eine Hilfsklasse kann eine Unterklasse einer abstrakten oder Hilfsklasse sein. Hilfsklassen können in der -Klasse nicht instanziiert Active Directory Domain Services. Eine Hilfsklasse kann eine beliebige Anzahl von Hilfsklassen in ihrer Definition enthalten. |



 

Verwechseln Sie **objectClassCategory nicht mit** einer [Objektkategorie.](object-class-and-object-category.md)

 

 




