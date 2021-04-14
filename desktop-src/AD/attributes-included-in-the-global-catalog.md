---
title: Einschließen von Attributen in den globalen Katalog
description: Der globale Katalog einer Gesamtstruktur enthält ein partielles Replikat aller Objekte in der Gesamtstruktur.
ms.assetid: 185467ed-7bcf-41e9-9862-02412009c437
ms.tgt_platform: multiple
keywords:
- Attribute, die im globalen Katalog AD enthalten sind
- Attribute ad, im globalen Katalog enthalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffbffd39e92456e6de7eccc6127f8a1351a4466
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472701"
---
# <a name="including-attributes-in-the-global-catalog"></a>Einschließen von Attributen in den globalen Katalog

Der globale Katalog einer Gesamtstruktur enthält ein partielles Replikat aller Objekte in der Gesamtstruktur. Der globale Katalog enthält für jedes Objekt nur eine Teilmenge der Attribute jedes Objekts. Das [**ismembership ofpartialattributeset**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) -Attribut eines [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts wird auf " **true** " festgelegt, wenn das Attribut in den globalen Katalog repliziert wird.

Attribute mit den folgenden Merkmalen eignen sich für den Speicher im globalen Katalog:

-   Das-Attribut ist Global interessant, da das-Attribut zum Suchen von Objekten erforderlich ist, die an beliebiger Stelle in der Gesamtstruktur vorkommen können, oder weil der Lesezugriff auf das Attribut wertvoll ist, auch wenn kein Zugriff auf das vollständige Objekt möglich ist. Ein Beispiel für den ersten Typ ist das [**Location**](/windows/desktop/ADSchema/a-location) -Attribut, das zum Suchen eines [**PrintQueue**](/windows/desktop/ADSchema/c-printqueue) -Objekts verwendet werden kann. Ein Beispiel für den zweiten Typ ist " [**telefonienumber**](/windows/desktop/ADSchema/a-telephonenumber)", da Sie jemanden auch dann aufrufen können, wenn Sie nicht auf ein vollständiges Replikat des [**Benutzer**](/windows/desktop/ADSchema/c-user) Objekts zugreifen können.
-   Die Volatilität des Attributs ist sehr gering. Dies ist wichtig, denn wenn eine Attribut Klasse im globalen Katalog enthalten ist, werden Änderungen an jedem Wert dieser Attribut Klasse in der gesamten Unternehmens Gesamtstruktur auf alle globalen Katalogserver im Unternehmen repliziert.
-   Die Größe des Attribut Werts ist klein. "Small" (klein) ist äußerst subjektiv: Beachten Sie beim Platzieren eines Attributs in den globalen Katalog die Auswirkung der Replikation des Attributs auf alle globalen Katalogserver im Unternehmen. Je kleiner das Attribut, desto niedriger die Auswirkung. Da die Replikation nur erfolgt, wenn sich das Attribut ändert, ist die Auswirkung der Replikation ebenfalls geringer, da die Volatilität abnimmt, sodass ein großes Attribut mit sehr geringer Volatilität möglicherweise eine geringere Gesamt Auswirkung als ein kleines Attribut mit hoher Volatilität hat.

Wenn Sie entscheiden, ob Sie ein Attribut in den globalen Katalog platzieren möchten, denken Sie daran, dass Sie eine höhere Replikation durchführen und den Datenträger Speicher auf globalen Katalog Servern für eine möglicherweise schnellere Abfrageleistung erhöhen. In der Regel verwenden Sie den globalen Katalog, um nach einem Objekt zu suchen, das von Interesse ist, um die ausgewählten Attribute des Objekts lesen zu können. Wenn die Attribute, an denen Sie interessiert sind, in den globalen Katalog repliziert werden, können Sie diese direkt aus dem globalen Katalog lesen. Zum Lesen von Attributen, die nicht in den globalen Katalog repliziert werden, müssen Sie alternativ weitere Schritte ausführen, um Sie abzurufen. In diesem Fall müssen Sie nach dem Durchsuchen des globalen Katalogs, um das gewünschte Objekt zu suchen, den Distinguished Name des Objekts aus dem globalen Katalog lesen, den DN zum direkten binden an ein vollständiges Replikat des Objekts verwenden, das sich möglicherweise auf einem anderen Server befindet, und schließlich die nicht globalen Katalog Attribute aus dem vollständigen Replikat des Objekts lesen.

Häufig abgefragte und referenzierte Attribute, wie z. b. Mitarbeiter Name und Telefonnummer, können im globalen Katalog enthalten sein. Ein Attribut, das nicht häufig referenziert wird, z. b. "DriverVersion" für Drucker, ist am besten aus dem globalen Katalog übrig.

 

 