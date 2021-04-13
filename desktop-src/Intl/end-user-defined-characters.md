---
description: Endbenutzer definierte Zeichen (EUDC) in Doppelbyte-Zeichensätzen (dbcss) und privaten Verwendungs Bereichs Zeichen (Pua) in Unicode sind benutzerdefinierte Zeichen.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Endbenutzer definierte und private Verwendungs Bereichs Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348139"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Endbenutzer definierte und private Verwendungs Bereichs Zeichen

Endbenutzer definierte Zeichen (EUDC) in [Doppelbyte-Zeichensätzen](double-byte-character-sets.md) (dbcss) und privaten Verwendungs Bereichs Zeichen (Pua) in [Unicode](unicode.md) sind benutzerdefinierte Zeichen. Sie können entweder von einem Endbenutzer oder von einer anderen Partei definiert und implementiert werden, z. b. von einem Gerätehersteller, einer Benutzergruppe, einem Regierungs Körper oder einem Schriftarten Entwurfs Unternehmen. Die Verwendung ermöglicht Benutzern das bilden von Namen und anderen Wörtern mithilfe von Zeichen, die nicht in den Standard Bildschirm-und Drucker Schriftarten verfügbar sind.

Die Zeichen EUDC und Pua können auf verschiedenen Computern anders zugewiesen oder überhaupt nicht zugewiesen werden. Einige Codepages verfügen über Erweiterungen, die den EUDC-Bereich wieder verwenden, und diese Erweiterungen können miteinander in Konflikt stehen. In anderen Fällen kann ein Hersteller einen benutzerdefinierten Satz von Zeichen in einem dieser Bereiche bereitstellen. Außerdem können Benutzergruppen versuchen, zusätzliche Zeichen im Pua anzugeben. Verschiedene Kombinationen dieser Fälle können zu Konflikten führen. Beim Erstellen von Anwendungen, die auf EUDC-oder Pua-Zeichen basieren, sollten Sie die in Konflikt stehenden Interpretationen eines einzelnen Code Punkts berücksichtigen.

In den folgenden Themen werden die Schriftarten erläutert, die eudcs unterstützen, sowie Zugriff und Verwaltung für diese Zeichen:

-   [Zeichensätze und Schriftarten](character-sets-and-fonts.md)
-   [EUDC-Registrierungseinträge](eudc-registry-entries.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Unicode und Zeichensätzen](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



