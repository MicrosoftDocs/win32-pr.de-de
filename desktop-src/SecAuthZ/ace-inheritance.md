---
description: Eine Objekt-ACL kann ACEs enthalten, die sie vom übergeordneten Container geerbt hat.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: ACE-Vererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd239801ea15dddb142c42d86e1aa44d0d644e5d217c50fc7c9cf9388747e45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785381"
---
# <a name="ace-inheritance"></a>ACE-Vererbung

Die ACL eines Objekts kann ACEs enthalten, die vom übergeordneten Container geerbt wurden. Beispielsweise kann ein Registrierungsunterschlüssel ACEs vom darüber liegenden Schlüssel in der Registrierungshierarchie erben. Ebenso kann eine Datei in einem NTFS-Dateisystem ACEs aus dem Verzeichnis erben, das sie enthält.

Die [**ACE \_ HEADER-Struktur**](/windows/desktop/api/Winnt/ns-winnt-ace_header) eines ACE enthält eine Reihe von Vererbungsflags, die die ACE-Vererbung und die Auswirkungen eines ACE auf das Objekt steuern, an das er angefügt ist. Das System interpretiert die Vererbungsflags und andere Vererbungsinformationen gemäß den [Regeln der ACE-Vererbung.](ace-inheritance-rules.md)

Diese Regeln wurden mit den folgenden Features erweitert:

-   Unterstützung für [die automatische Weitergabe vererbbarer ACEs.](automatic-propagation-of-inheritable-aces.md)
-   Ein Flag, das zwischen geerbten ACEs und ACEs unterscheidet, die direkt auf ein Objekt angewendet wurden.
-   Objektspezifische ACEs, mit denen Sie den Typ des untergeordneten Objekts angeben können, das den ACE erben kann.
-   Die Möglichkeit, zu verhindern, dass eine DACL oder SACL ACEs erbt, indem die SE \_ DACL \_ PROTECTED- oder SE \_ SACL \_ PROTECTED-Bits in den [*Steuerungsbits des Sicherheitsdeskriptors*](/windows/desktop/SecGloss/s-gly) mit Ausnahme von SYSTEM \_ RESOURCE ATTRIBUTE ACE und SYSTEM \_ SCOPED POLICY ID \_ \_ \_ \_ \_ ACE festgelegt werden.

 

 
