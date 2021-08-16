---
description: Das System gibt vererbbare Zugriffssteuerungseinträge (ACEs) gemäß einer Reihe von Vererbungsregeln an untergeordnete Objekte weiter.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: ACE-Vererbungsregeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba77e5d9fcbef9125108e8f0be76cd5b7c79a2f99ba524c81f3fd1da84336f04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785363"
---
# <a name="ace-inheritance-rules"></a>ACE-Vererbungsregeln

Das System gibt vererbbare [](/windows/desktop/SecGloss/a-gly) Zugriffssteuerungseinträge (ACEs) gemäß einer Reihe von Vererbungsregeln an untergeordnete Objekte weiter. Das System platziert geerbte ACEs in der DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) des untergeordneten -Steuerelements gemäß der bevorzugten Reihenfolge von [ACEs in einer DACL.](order-of-aces-in-a-dacl.md) Das System legt das FLAG INHERITED \_ ACE in allen geerbten ACEs fest.

Die acEs, die von untergeordneten Containerobjekten und untergeordneten Nichtcontainerobjekten geerbt werden, unterscheiden sich abhängig von den Kombinationen von Vererbungsflags. Diese Vererbungsregeln funktionieren für DACLs und [*Systemzugriffssteuerungslisten*](/windows/desktop/SecGloss/s-gly) (SACLs) gleich.



| Übergeordnetes ACE-Flag                                  | Auswirkung auf die untergeordnete ACL                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nur OBJECT \_ INHERIT \_ ACE                        | Untergeordnete Objekte ohne Container: Geerbt als effektiver ACE. Untergeordnete Containerobjekte: Container erben einen ACE, der nur erbt, es sei denn, das BITflag NO \_ PROPAGATE \_ INHERIT ACE ist ebenfalls \_ festgelegt.<br/>                                       |
| NUR CONTAINER \_ INHERIT \_ ACE                     | Untergeordnete Objekte ohne Container: Keine Auswirkung auf das untergeordnete Objekt. Untergeordnete Containerobjekte: Das untergeordnete Objekt erbt einen effektiven ACE. Der geerbte ACE ist vererbbar, es sei denn, das NO \_ PROPAGATE \_ INHERIT \_ ACE-Bitflag ist ebenfalls festgelegt.<br/> |
| CONTAINER \_ INHERIT ACE und OBJECT INHERIT \_ \_ \_ ACE | Untergeordnete Objekte ohne Container: Geerbt als effektiver ACE. Untergeordnete Containerobjekte: Das untergeordnete Objekt erbt einen effektiven ACE. Der geerbte ACE ist vererbbar, es sei denn, das NO \_ PROPAGATE \_ INHERIT \_ ACE-Bitflag ist ebenfalls festgelegt.<br/> |
| Keine Vererbungsflags festgelegt                         | Keine Auswirkung auf untergeordnete Container oder Nichtcontainerobjekte.                                                                                                                                                                                    |



 

Wenn ein geerbter ACE ein effektiver ACE für das untergeordnete Objekt ist, ordnet das System alle generischen Rechte den spezifischen Rechten für das untergeordnete Objekt zu. Auf ähnliche Weise ordnet [](/windows/desktop/SecGloss/s-gly) das System generische Sicherheits-IDs (SIDs) wie CREATOR \_ OWNER der entsprechenden SID zu. Wenn es sich bei einem geerbten ACE um einen ace handelt, der nur geerbt wird, bleiben alle generischen Rechte oder generischen SIDs unverändert, sodass sie entsprechend zugeordnet werden können, wenn der ACE von der nächsten Generation untergeordneter Objekte geerbt wird.

Für einen Fall, in dem ein Containerobjekt einen ACE erbt, der sowohl für den Container gilt als auch von seinen Nachfolgern vererbt werden kann, kann der Container zwei ACEs erben. Dies tritt auf, wenn der vererbbare ACE generische Informationen enthält. Der Container erbt einen nur erbenden ACE, der die generischen Informationen enthält, und einen effektiven ACE, in dem die generischen Informationen zugeordnet wurden.

Ein [objektspezifischer ACE verfügt](object-specific-aces.md) über einen **InheritedObjectType-Member,** der eine GUID enthalten kann, um den Typ des Objekts zu identifizieren, das den ACE erben kann.

Wenn die **InheritedObjectType-GUID** nicht angegeben ist, sind die Vererbungsregeln für einen objektspezifischen ACE mit den Vererbungsregeln für einen Standard-ACE identisch.

Wenn die **InheritedObjectType-GUID** angegeben wird, kann der ACE von Objekten geerbt werden, die mit der GUID übereinstimmen, wenn OBJECT INHERIT ACE festgelegt ist, und von Containern, die mit der GUID übereinstimmen, wenn CONTAINER INHERIT ACE festgelegt \_ \_ \_ \_ ist. Beachten Sie, dass derzeit nur DS-Objekte objektspezifische ACEs unterstützen und der DS alle Objekttypen als Container behandelt.

 

