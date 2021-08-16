---
description: Unabhängig davon, ob Sie Ihre MTS-Pakete manuell in COM+-Anwendungen konvertieren oder den Microsoft Windows-Setupprozess automatisch ausführen lassen, sollten Sie die Ergebnisse der Konvertierung sowie die Probleme kennen.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: COM+-Konvertierungsergebnisse und -probleme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a347df5f0ad0b16aee509c9c1b2c2c848372d0df2ccbc376814b0d14eb61d138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129212"
---
# <a name="com-conversion-results-and-issues"></a>COM+-Konvertierungsergebnisse und -probleme

Unabhängig davon, ob Sie Ihre MTS-Pakete manuell in COM+-Anwendungen konvertieren oder den Microsoft Windows-Setupprozess automatisch ausführen lassen, sollten Sie die Ergebnisse der Konvertierung sowie die Probleme kennen.

## <a name="what-is-converted"></a>Was wird konvertiert?

Während der Konvertierung konvertiert das MTSTOCOM-Hilfsprogramm Rollen, Rollenzuweisungen, Schnittstellen, Methoden, Benutzer, die Computerliste und die meisten Computereinstellungen. Das MTSTOCOM-Hilfsprogramm konvertiert auch die Identität und das Kennwort für ein MTS-Paket.

Die neuen COM+-Attribute, die in MTS nicht verfügbar waren, werden für alle konvertierten MTS-Komponenten automatisch auf die folgenden Standardwerte festgelegt. Diese Standardwerte können entweder mit dem Component Services-Verwaltungstool oder den COM+-Verwaltungsschnittstellen geändert werden.

-   JIT-Aktivierung aktiviert.
-   Objektpooling deaktiviert.
-   Die Synchronisierung ist identisch mit der Transaktionseinstellung.

## <a name="conversion-issues"></a>Konvertierungsprobleme

COM+ wird automatisch installiert, wenn Sie Windows. Com+ kann nicht deinstalliert werden. Probleme im Zusammenhang mit Upgrades vorhandener MTS- und COM+-Installationen umfassen Folgendes:

-   Wenn Sie derzeit MTS 1.0 verwenden, wird MTS automatisch auf COM+ aktualisiert. Benutzerdefinierte Pakete gehen jedoch verloren, und Sie müssen sie neu erstellen.
-   Wenn Sie derzeit MTS 2.0 verwenden, wird MTS automatisch auf COM+ aktualisiert. Alle benutzerdefinierten Pakete werden auf COM+-Anwendungen aktualisiert. Alle Komponenten sollten wie unter MTS 2.0 funktionieren.
-   Wenn Sie MTS 1.0 und MTS 2.0 verwenden und die SDK-Option installiert haben, werden die SDK-Dateien entfernt. Sie können das neueste COM+-SDK über das Microsoft Windows SDK installieren.
-   Sie können einen MTS-Remotecomputer nicht über einen COM+-Computer verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Automatische Konvertierung von MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Manuelle Konvertierung von MTS](manual-conversion-from-mts.md)
</dt> <dt>

[MTS-Verwaltungsbibliothek](mts-administration-library.md)
</dt> </dl>

 

 



