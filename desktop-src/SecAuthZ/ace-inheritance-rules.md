---
description: Das System gibt nach einem Satz von Vererbungs Regeln vererbbare Zugriffs Steuerungs Einträge (ACEs) an untergeordnete Objekte weiter.
ms.assetid: 08f76aaa-8379-4ba8-9735-7568001bcd53
title: ACE-Vererbungs Regeln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8c786ebcc8450e8e5da1833f34fc85c37ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756193"
---
# <a name="ace-inheritance-rules"></a>ACE-Vererbungs Regeln

Das System gibt nach einem Satz von Vererbungs Regeln vererbbare [*Zugriffs Steuerungs Einträge*](/windows/desktop/SecGloss/a-gly) (ACEs) an untergeordnete Objekte weiter. Das System stellt geerbte ACEs in der freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des untergeordneten Elements gemäß der bevorzugten [Reihenfolge von ACEs in einer DACL](order-of-aces-in-a-dacl.md)dar. Das System legt das geerbte \_ ACE-Flag in allen geerbten ACEs fest.

Die von Container und untergeordneten nicht Container-Objekten geerbten ACEs unterscheiden sich abhängig von den Kombinationen von Vererbungs Flags. Diese Vererbungs Regeln funktionieren für DACLs und System- [*Zugriffs Steuerungs Listen*](/windows/desktop/SecGloss/s-gly) (SACLs) identisch.



| Übergeordnetes ACE-Flag                                  | Auswirkung auf untergeordnete ACL                                                                                                                                                                                                                      |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Nur Objekt erben ( \_ ACE)                        | Untergeordnete nicht Containerobjekte: als effektiver ACE geerbt. Untergeordnete Containerobjekte: Container erben einen nur Erben-ACE, es sei denn, das No \_ propagieren- \_ ACE- \_ Bitflag ist ebenfalls festgelegt.<br/>                                       |
| \_Nur Container erben \_                     | Untergeordnete nicht Containerobjekte: keine Auswirkung auf das untergeordnete Objekt. Untergeordnete Container Objekte: das untergeordnete Objekt erbt einen effektiven ACE. Der geerbte ACE ist vererbbar, es sei denn, es \_ ist auch das No propagieren- \_ ACE- \_ Bitflag<br/> |
| Container \_ erben \_ ACE und Objekt \_ Vererbung \_ | Untergeordnete nicht Containerobjekte: als effektiver ACE geerbt. Untergeordnete Container Objekte: das untergeordnete Objekt erbt einen effektiven ACE. Der geerbte ACE ist vererbbar, es sei denn, es \_ ist auch das No propagieren- \_ ACE- \_ Bitflag<br/> |
| Keine Vererbungs Flags festgelegt.                         | Keine Auswirkung auf untergeordnete Container-oder nicht Container-Objekte.                                                                                                                                                                                    |



 

Wenn ein geerbte ACE ein effektiver ACE für das untergeordnete Objekt ist, ordnet das System alle generischen Rechte den spezifischen Rechten für das untergeordnete Objekt zu. Ebenso ordnet das System generische [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs), z. b. Ersteller- \_ Besitzer, der entsprechenden sid zu. Wenn es sich bei einem geerbten ACE um einen Vererbungs-ACE handelt, bleiben alle generischen Rechte oder generischen SIDs unverändert, sodass Sie ordnungsgemäß zugeordnet werden können, wenn der ACE von der nächsten Generation von untergeordneten Objekten geerbt wird.

Für einen Fall, in dem ein Container Objekt einen ACE erbt, der sowohl für den Container gültig ist als auch durch seine Nachfolger vererbt werden kann, erbt der Container möglicherweise zwei ACEs. Dies tritt auf, wenn der vererbbare ACE generische Informationen enthält. Der Container erbt einen reinen Vererbungs-ACE, der die generischen Informationen und einen effektiven ACE enthält, in dem die generischen Informationen zugeordnet wurden.

Ein [Objekt spezifischer ACE](object-specific-aces.md) weist einen **vereritedobjecttype** -Member auf, der eine GUID enthalten kann, um den Typ des Objekts zu identifizieren, das den ACE erben kann.

Wenn die GUID " **eritedobjecttype** " nicht angegeben wird, sind die Vererbungs Regeln für einen Objekt spezifischen ACE identisch mit denen für einen Standard-ACE.

Wenn die GUID **erbt** , wird der ACE von Objekten vererbt, die der GUID entsprechen, wenn der Objekt \_ Vererbungs- \_ ACE festgelegt ist, und von Containern, die der GUID entsprechen, wenn der Container \_ Vererbungs- \_ ACE festgelegt ist. Beachten Sie, dass derzeit nur DS-Objekte objektspezifische ACEs unterstützen, und die DS alle Objekttypen als Container behandelt.

 

