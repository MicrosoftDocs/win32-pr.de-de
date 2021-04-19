---
description: ICE39 überprüft den Zusammenfassungs Informationsdaten Strom der Datenbank.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358566"
---
# <a name="ice39"></a>ICE39

ICE39 überprüft den [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) der Datenbank.

ICE39 überprüft das Format der folgenden Eigenschaften:

-   [**Zusammenfassung der Wort Zählung**](word-count-summary.md)
-   [**Zusammenfassung der Seitenanzahl**](page-count-summary.md)
-   [**Vorlagen Zusammenfassung**](template-summary.md)
-   [**Zusammenfassung der Revisionsnummer**](revision-number-summary.md)
-   [**Zeit-/datezusammenfassung erstellen**](create-time-date-summary.md)
-   [**Zusammenfassung der letzten gespeicherten Zeit/Datum**](last-saved-time-date-summary.md)
-   [**Letzte gedruckte Zusammenfassung**](last-printed-summary.md)

Wenn die Eigenschaft für die [**Wort Zähl Zusammenfassung**](word-count-summary.md) angibt, dass die Quelle komprimiert ist, gibt ICE39 eine Warnung aus, wenn in der Spalte Attribute der [Dateitabelle](file-table.md)auch Dateien als komprimiert gekennzeichnet werden. Siehe [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).

ICE39 gibt eine Warnung aus, wenn die [**Wort Zählung-Zusammenfassungs**](word-count-summary.md) Eigenschaft angibt, dass das Paket UAC-kompatibel ist und die [msipackagecertificate-Tabelle](msipackagecertificate-table.md) nicht leer ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



