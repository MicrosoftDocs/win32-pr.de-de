---
title: Bestimmen der klassen, die einer Objektinstanz zugeordnet sind
description: Jedes Objekt in Active Directory Domain Services verfügt über zwei Attribute, deren Werte die Hierarchie der Objektklassen identifizieren, deren -Objekt eine -Instanz ist.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af65b5e1abf7f0bc68ae115cb409d2cdb556e08
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471496"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Bestimmen der klassen, die einer Objektinstanz zugeordnet sind

Jedes Objekt in Active Directory Domain Services verfügt über zwei Attribute, deren Werte die Hierarchie der Objektklassen identifizieren, deren -Objekt eine -Instanz ist.




| Attribut | BESCHREIBUNG | 
|-----------|-------------|
| <strong>structuralObjectClass</strong> | Identifiziert die strukturellen und abstrakten Klassen, deren -Objekt eine -Instanz ist. Die Werte für ein Benutzerobjekt können z. B.:<ul><li><strong>top</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 
| <strong>Objectclass</strong> | Identifiziert die klassen, die in <strong>structuralObjectClass</strong>enthalten sind, sowie alle Hilfsklassen, die dynamisch angefügt werden. Wenn z. B. eine "Fahrzeug"-Hilfsklasse an ein Benutzerobjekt angefügt ist, können die Folgenden Werte verwendet werden:<ul><li><strong>top</strong></li><li><strong>Fahrzeug</strong></li><li><strong>person</strong></li><li><strong>organizationalPerson</strong></li><li><strong>user</strong></li></ul> | 




 

Beachten Sie, dass keines dieser Attribute Hilfsklassen enthält, die statisch mit den Objektklassen verknüpft sind, deren -Objekt eine -Instanz ist. Beispielsweise ist die Hilfsklasse **securityPrincipal** statisch mit der **Benutzerklasse** verknüpft, da sie in den **systemAuxiliaryClass-Werten** des **BenutzerklasseSchema-Objekts** enthalten ist. sie ist weder in den **objectClass-** noch in den **structuralObjectClass-Attributen** von Instanzen der Benutzerklasse enthalten.

 

 




