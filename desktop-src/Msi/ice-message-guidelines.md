---
description: Benutzerdefinierte ICE-Aktionen kommunizieren, indem MsiProcessMessage aufgerufen und eine NACHRICHT vom Typ INSTALLMESSAGE \_ USER gepostet wird.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: RICHTLINIEN für ICE-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d603175dbecc12b0b9524db1a02d9ca677f61c87
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887449"
---
# <a name="ice-message-guidelines"></a>RICHTLINIEN für ICE-Nachrichten

Benutzerdefinierte ICE-Aktionen kommunizieren, indem [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) aufgerufen und eine NACHRICHT vom Typ INSTALLMESSAGE \_ USER gepostet wird.

Formatieren Sie die Zeichenfolge beim Erstellen einer Meldungszeichenfolge für eine benutzerdefinierte ICE-Aktion wie folgt.

*Name des ICE* &lt; registerkarte &gt; *Registerkarte Nachrichtentyp* &lt; Registerkarte &gt; *Beschreibung* &lt; Registerkarte &gt; *Hilfe-URL oder Speicherort* Registerkarte &lt; &gt; *Tabellenname* Registerkarte &lt; &gt; *Spaltenname* Registerkarte &lt; &gt; *Primärschlüssel* Registerkarte &lt; &gt; *Primärschlüssel* Registerkarte &lt; &gt; *Primärschlüssel* . . . (Wiederholen Sie den Vorgang für so viele Primärschlüssel wie erforderlich.)

Die ersten drei Felder der Zeichenfolge sind in jeder Nachricht erforderlich.

Das Feld Nachrichtentyp gibt an, ob der ICE eine Fehler-, Fehler-, Warnungs- oder Informationsmeldung meldet.



| Wert | Nachrichtentyp                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fehlermeldung, die den Fehler der benutzerdefinierten ICE-Aktion meldet.                                                                                                       |
| 1     | Fehlermeldung, die die Datenbankerstellung meldet, die ein falsches Verhalten verursacht.                                                                                             |
| 2     | Warnmeldung, die die Datenbankerstellung meldet, die in bestimmten Fällen zu falschem Verhalten führt. Warnungen können auch unerwartete Nebeneffekte der Datenbankerstellung melden. |
| 3     | Informationsmeldung.                                                                                                                                                |



 

Wenn die Hilfe nicht verfügbar ist, kann das Feld Hilfe-URL die leere Zeichenfolge sein.

Fehler- und Warnmeldungen sollten die Felder Tabellenname, Spaltenname und Primärschlüssel enthalten. Wenn eines dieser Felder ausgelassen wird, müssen alle Felder, die auf das erste leere Feld folgen, aus der Nachricht weggelassen werden. Beispielsweise wird ein Tabellenname ohne Spaltenname und Primärschlüssel oder tabellenname bereitgestellt, und ein Spaltenname wird ohne Primärschlüssel bereitgestellt. Ein Spaltenname und Primärschlüssel können jedoch nicht ohne Tabellenname verwendet werden. Es können mehrere Primärschlüssel aufgelistet werden, bis alle Primärschlüssel in dieser Tabelle Werte erhalten haben.

## <a name="examples"></a>Beispiele

Die erste Meldung, die durch das [Beispiel-ICE in C++](sample-ice-in-c-.md)veranschaulicht wird:

"ICE01 \\ t3 \\ tCreated 04/29/1998 by <insert author es name here>."

Die zweite Vom ICE-Beispiel gepostete Nachricht:

"ICE01 \\ t3 \\ tLast modified 05/06/1999 by <insert author es name here>."

Die dritte Vom ICE-Beispiel gepostete Nachricht.

"ICE01 \\ t3 \\ tSimple ICE to illustrating the ICE concept" (ICE01 t3 tSimple ICE zur Veranschaulichung des ICE-Konzepts)

 

 



