---
description: Eine Objekt-ACL kann ACEs enthalten, die Sie von ihrem übergeordneten Container geerbt hat.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: ACE-Vererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959484"
---
# <a name="ace-inheritance"></a>ACE-Vererbung

Die ACL eines Objekts kann ACEs enthalten, die es von seinem übergeordneten Container geerbt hat. Beispielsweise kann ein Registrierungs Unterschlüssel ACEs von dem übergeordneten Schlüssel in der Registrierungs Hierarchie erben. Ebenso kann eine Datei in einem NTFS-Dateisystem ACEs von dem Verzeichnis erben, in dem Sie enthalten ist.

Die [**ACE- \_ Header**](/windows/desktop/api/Winnt/ns-winnt-ace_header) Struktur eines ACE enthält einen Satz von Vererbungsflags, die die ACE-Vererbung steuern, und die Auswirkung eines ACE auf das Objekt, an das Sie angefügt ist. Das System interpretiert die Vererbungs Flags und andere Vererbungs Informationen gemäß den [Regeln für die ACE-Vererbung](ace-inheritance-rules.md).

Diese Regeln wurden durch die folgenden Features erweitert:

-   Unterstützung für die [Automatische Propagierung von vererbbaren ACEs](automatic-propagation-of-inheritable-aces.md).
-   Ein Flag, das zwischen geerbten ACEs und ACEs unterscheidet, die direkt auf ein Objekt angewendet wurden.
-   Objektspezifische ACEs, die es Ihnen ermöglichen, den Typ des untergeordneten Objekts anzugeben, das den ACE erben kann.
-   Die Möglichkeit, zu verhindern, dass eine DACL oder SACL ACEs erbt, indem die von SE \_ DACL \_ geschützten oder SE \_ SACL \_ -geschützten Bits in den Steuerelementen der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) festgelegt werden, mit Ausnahme des System \_ Ressourcen \_ Attribut \_ ACE und der \_ Richtlinien-ID ACE für systemweite \_ Richtlinien \_ \_ .

 

 
