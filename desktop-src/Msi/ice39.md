---
description: ICE39 überprüft den Zusammenfassungsinformationsstream der Datenbank.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb912afbe7220eee1aa3bbcd494f6531736279b85c5736f6867fdf8779e39bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528440"
---
# <a name="ice39"></a>ICE39

ICE39 überprüft den [Zusammenfassungsinformationsstream](summary-information-stream.md) der Datenbank.

ICE39 überprüft das Format der folgenden Eigenschaften:

-   [**Zusammenfassung der Wortanzahl**](word-count-summary.md)
-   [**Zusammenfassung der Seitenanzahl**](page-count-summary.md)
-   [**Vorlagenzusammenfassung**](template-summary.md)
-   [**Zusammenfassung der Revisionsnummer**](revision-number-summary.md)
-   [**Erstellen einer Zeit-/Datumszusammenfassung**](create-time-date-summary.md)
-   [**Zuletzt gespeicherte Uhrzeit/Datumszusammenfassung**](last-saved-time-date-summary.md)
-   [**Zuletzt gedruckte Zusammenfassung**](last-printed-summary.md)

Wenn die [**Zusammenfassungseigenschaft**](word-count-summary.md) der Wortanzahl angibt, dass die Quelle komprimiert ist, gibt ICE39 eine Warnung aus, wenn Dateien auch in der Spalte Attribute der Dateitabelle als komprimiert [markiert sind.](file-table.md) Weitere Informationen [finden Sie unter Verwenden von Schränken und komprimierten Quellen.](using-cabinets-and-compressed-sources.md)

ICE39 gibt eine [](word-count-summary.md) Warnung aus, wenn die Zusammenfassungseigenschaft der Wortanzahl angibt, dass das Paket UAC-kompatibel ist und die [MsiPackageCertificate-Tabelle](msipackagecertificate-table.md) nicht leer ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



