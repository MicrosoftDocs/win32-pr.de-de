---
description: Benutzerdefinierte Ice-Aktionen kommunizieren durch Aufrufen von "msiprocessmessage" und Veröffentlichen einer installmessage- \_ benutzertypnachricht.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Richtlinien für ICE Message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958887"
---
# <a name="ice-message-guidelines"></a>Richtlinien für ICE Message

Benutzerdefinierte Ice-Aktionen kommunizieren durch Aufrufen von " [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) " und Veröffentlichen einer installmessage- \_ benutzertypnachricht.

Beim Erstellen einer Meldungs Zeichenfolge für eine benutzerdefinierte Ice-Aktion formatieren Sie die Zeichenfolge wie folgt.

*Name des ICE* <tab> *Nachrichtentyp* <tab> *Beschreibung* <tab> *Hilfe-URL oder-Speicherort* <tab> *Tabellen Name* <tab> *Spalten Name* <tab> *Primärschlüssel* <tab> *Primärschlüssel* <tab> *Primärschlüssel* . . . (wiederholen Sie dies bei Bedarf für so viele Primärschlüssel).

Die ersten drei Felder der Zeichenfolge sind in jeder Nachricht erforderlich.

Das Feld Nachrichtentyp gibt an, ob das Ice einen Fehler, Fehler, eine Warnung oder eine Informations Meldung meldet.



| Wert | Nachrichtentyp                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fehlermeldung, die den Fehler der benutzerdefinierten Ice-Aktion meldet.                                                                                                       |
| 1     | Fehlermeldungs Berichterstellung der Datenbank, die falsches Verhalten verursachen.                                                                                             |
| 2     | Warnmeldung Berichterstellung der Datenbank, die in bestimmten Fällen falsches Verhalten verursacht. Warnungen können auch unerwartete Nebeneffekte der Daten Bank Erstellung melden. |
| 3     | Informationsmeldung.                                                                                                                                                |



 

Wenn die Hilfe nicht verfügbar ist, kann das Feld "Hilfe-URL" eine leere Zeichenfolge sein.

Fehler-und Warnmeldungen sollten den Tabellennamen, Spaltennamen und Primärschlüssel Felder bereitstellen. Wenn eines dieser Felder weggelassen wird, müssen alle Felder, die dem ersten leeren Feld folgen, nicht aus der Nachricht entfernt werden. Beispielsweise wird ein Tabellenname ohne einen Spaltennamen und Primärschlüssel oder einen Tabellennamen bereitgestellt, und ein Spaltenname wird ohne Primärschlüssel bereitgestellt. Ein Spaltenname und Primärschlüssel können jedoch nicht ohne einen Tabellennamen verwendet werden. Es können mehrere Primärschlüssel aufgelistet werden, bis allen primär Schlüsseln in dieser Tabelle Werte zugewiesen wurden.

## <a name="examples"></a>Beispiele

Die erste Meldung, die durch das [Sample Ice in C++](sample-ice-in-c-.md)veranschaulicht wird:

"ICE01 \\ T3 \\ tcreated 04/29/1998 by <hier den Namen des Autors einfügen>."

Die zweite Nachricht, die von dem Sample Ice gepostet wurde:

"ICE01 \\ T3 \\ tlast modified 05/06/1999 by <hier den Namen des Autors einfügen>."

Die dritte Nachricht, die von dem Sample Ice gepostet wurde.

"ICE01 \\ T3 \\ tsimple Ice, um das eiskonzept zu veranschaulichen".

 

 



