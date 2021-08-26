---
description: Benutzerdefinierte Zeichen (EUDC) in Doppel-Byte-Zeichensätzen (DBCSs) und PUA-Zeichen (Private Use Area) in Unicode sind benutzerdefinierte Zeichen.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Benutzerdefinierte und private Verwendungsbereichszeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19152ff8564cae4ccccc154a6c9d349f0fc6cd8791fcccb1973b553bc681cc5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898759"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Benutzerdefinierte und private Verwendungsbereichszeichen

Benutzerdefinierte Zeichen (EUDC) in Doppel-Byte-Zeichensätzen (DBCSs) und PUA-Zeichen (Private Use Area) in [Unicode](unicode.md) sind benutzerdefinierte Zeichen. [](double-byte-character-sets.md) Sie können entweder von einem Endbenutzer oder von einer anderen Partei definiert und implementiert werden, z. B. von einem Gerätehersteller, einer Benutzergruppe, einer Regierungsstelle oder einem Schriftentwurfsunternehmen. Durch ihre Verwendung können Benutzer Namen und andere Wörter mit Zeichen formen, die in Standardbildschirm- und Druckerschriftarten nicht verfügbar sind.

Die EUDC- und PUA-Zeichen können auf verschiedenen Computern unterschiedlich oder überhaupt nicht zugewiesen werden. Einige Codepages verfügen über Erweiterungen, die den EUDC-Bereich wiederverwenden, und diese Erweiterungen können miteinander in Konflikt stehen. In anderen Fällen kann ein Hersteller einen benutzerdefinierten Zeichensatz in einem dieser Bereiche bereitstellen. Darüber hinaus können Benutzergruppen versuchen, zusätzliche Zeichen im PUA zur Verfügung zu stellen. Verschiedene Kombinationen dieser Fälle können zu Konflikten führen. Beim Erstellen von Anwendungen, die auf EUDC- oder PUA-Zeichen basieren, sollten Sie die in Konflikt stehenden Interpretationen eines einzelnen Codepunkts berücksichtigen.

In den folgenden Themen werden die Schriftarten, die EUDCs unterstützen, sowie der Zugriff und die Verwaltung für diese Zeichen behandelt:

-   [Zeichensätze und Schriftarten](character-sets-and-fonts.md)
-   [EUDC-Registrierungseinträge](eudc-registry-entries.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Unicode und Zeichensätzen](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



