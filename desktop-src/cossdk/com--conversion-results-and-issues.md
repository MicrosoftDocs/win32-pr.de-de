---
description: Unabhängig davon, ob Sie Ihre MTS-Pakete manuell in com+-Anwendungen konvertieren oder Sie vom Microsoft Windows Setup-Prozess automatisch ausführen lassen, sollten Sie sich über die Ergebnisse der Konvertierung und die Probleme informieren.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Ergebnisse und Probleme bei der com+-Konvertierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393234"
---
# <a name="com-conversion-results-and-issues"></a>Ergebnisse und Probleme bei der com+-Konvertierung

Unabhängig davon, ob Sie Ihre MTS-Pakete manuell in com+-Anwendungen konvertieren oder Sie vom Microsoft Windows Setup-Prozess automatisch ausführen lassen, sollten Sie sich über die Ergebnisse der Konvertierung und die Probleme informieren.

## <a name="what-is-converted"></a>Was konvertiert wird

Während der Konvertierung konvertiert das Dienstprogramm mtstocom Rollen, Rollenzuweisungen, Schnittstellen, Methoden, Benutzer, die Computer Liste und die meisten Computereinstellungen. Das Dienstprogramm mtstocom konvertiert außerdem die Identität und das Kennwort für ein MTS-Paket.

Die neuen com+-Attribute, die in MTS nicht verfügbar waren, werden automatisch auf die folgenden Standardwerte für alle konvertierten MTS-Komponenten festgelegt. Diese Standardeinstellungen können entweder mit dem Verwaltungs Programmkomponenten Dienste oder mit den administrativen Verwaltungs Schnittstellen von com+ geändert werden.

-   Die JIT-Aktivierung ist aktiviert.
-   Objekt Pooling deaktiviert.
-   Synchronisierung identisch mit der Transaktions Einstellung.

## <a name="conversion-issues"></a>Konvertierungsprobleme

Com+ wird automatisch installiert, wenn Sie Windows installieren. Es ist nicht möglich, com+ zu deinstallieren. Probleme im Zusammenhang mit Upgrades vorhandener MTS-und com+-Installationen umfassen Folgendes:

-   Wenn Sie zurzeit MTS 1,0 verwenden, wird MTS automatisch auf com+ aktualisiert. Benutzerdefinierte Pakete gehen jedoch verloren und müssen neu erstellt werden.
-   Wenn Sie zurzeit MTS 2,0 verwenden, wird MTS automatisch auf com+ aktualisiert. Alle benutzerdefinierten Pakete werden auf COM+-Anwendungen aktualisiert. Alle Komponenten sollten wie unter MTS 2,0 funktionieren.
-   Wenn Sie die Optionen MTS 1,0 und MTS 2,0 verwenden und die SDK-Option installiert haben, werden die SDK-Dateien entfernt. Sie können das aktuelle com+-SDK über die Microsoft Windows SDK installieren.
-   Sie können einen Remote Computer mit dem Computer nicht von einem com+-Computer aus verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Automatische Konvertierung von MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Manuelle Konvertierung von MTS](manual-conversion-from-mts.md)
</dt> <dt>

[MTS-Verwaltungs Bibliothek](mts-administration-library.md)
</dt> </dl>

 

 



