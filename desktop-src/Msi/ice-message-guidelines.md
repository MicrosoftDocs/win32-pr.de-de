---
description: Benutzerdefinierte ICE-Aktionen kommunizieren durch Aufrufen von MsiProcessMessage und Senden einer Nachricht vom Typ INSTALLMESSAGE \_ USER.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: RICHTLINIEN für ICE-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0951f8573fce1b9dbe81b107fba2f2beb674ed063fae53182a7d2694ded35abb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821670"
---
# <a name="ice-message-guidelines"></a>RICHTLINIEN für ICE-Nachrichten

Benutzerdefinierte ICE-Aktionen kommunizieren durch Aufrufen [**von MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) und Senden einer Nachricht vom Typ INSTALLMESSAGE \_ USER.

Formatieren Sie die Zeichenfolge beim Erstellen einer Meldungszeichenfolge für eine benutzerdefinierte ICE-Aktion wie folgt.

*Name des ICE* <tab> *Nachrichtentyp* <tab> *Beschreibung* <tab> *Hilfe-URL oder Speicherort* <tab> *Tabellenname* <tab> *Spaltenname* <tab> *Primärschlüssel* <tab> *Primärschlüssel* <tab> *Primärschlüssel* . . . (Wiederholen Sie dies für so viele Primärschlüssel wie erforderlich))

Die ersten drei Felder der Zeichenfolge sind in jeder Nachricht erforderlich.

Das Feld Nachrichtentyp gibt an, ob der ICE eine Fehler-, Fehler-, Warnungs- oder Informationsmeldung meldet.



| Wert | Nachrichtentyp                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fehlermeldung, die den Fehler der benutzerdefinierten ICE-Aktion berichtet.                                                                                                       |
| 1     | Fehlermeldung bei der Datenbankerstellung, die ein falsches Verhalten verursacht.                                                                                             |
| 2     | Warnmeldung zur Datenbankerstellung, die in bestimmten Fällen ein falsches Verhalten verursacht. Warnungen können auch unerwartete Nebeneffekte der Datenbankerstellung melden. |
| 3     | Informationsmeldung.                                                                                                                                                |



 

Wenn keine Hilfe verfügbar ist, kann das Feld Hilfe-URL die leere Zeichenfolge sein.

Fehler- und Warnmeldungen sollten die Felder Tabellenname, Spaltenname und Primärschlüssel enthalten. Wenn eines dieser Felder ausgelassen wird, müssen alle Felder, die auf das erste leere Feld folgen, nicht in der Meldung enthalten sein. Beispielsweise wird ein Tabellenname ohne Spaltenname und Primärschlüssel oder tabellenname bereitgestellt, und es wird ein Spaltenname ohne Primärschlüssel bereitgestellt. Ein Spaltenname und Primärschlüssel können jedoch nicht ohne einen Tabellennamen verwendet werden. Es können mehrere Primärschlüssel aufgelistet werden, bis alle Primärschlüssel in dieser Tabelle Werte erhalten haben.

## <a name="examples"></a>Beispiele

Die erste Meldung, die im [Beispiel-ICE in C++ veranschaulicht wird:](sample-ice-in-c-.md)

"ICE01 \\ t3 \\ tCreated 04/29/1998 by <insert author es name here>."

Die zweite Nachricht, die vom Beispiel-ICE gepostet wurde:

"ICE01 \\ t3 \\ tLast modified 05/06/1999 by <insert author es name here>."

Die dritte Nachricht, die vom Beispiel-ICE gepostet wurde.

"ICE01 \\ t3 \\ tSimple ICE zur Veranschaulichung des ICE-Konzepts".

 

 



