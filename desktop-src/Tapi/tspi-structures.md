---
description: Die Von TSPI-Datenstrukturen verwendeten Datenstrukturen sind identisch mit denen, die in TAPI-Strukturen definiert sind, mit Ausnahme von TSISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: TSPI-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c11700dcaa46284b4050908ca70ed640e03afeb2eb7a2269ad1bac9161c089
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139753"
---
# <a name="tspi-structures"></a>TSPI-Strukturen

Die Datenstrukturen, die TSPI verwendet, sind identisch mit denen, die in [TAPI-Strukturen](./tapi-structures.md)definiert sind, mit Ausnahme von [**TSISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).

Bei den meisten größeren Datenstrukturen wird die Verantwortung für das Ausfüllen von Membern auf den Dienstanbieter und TAPI aufgeteilt. Der Dienstanbieter muss die Werte beibehalten, die in Mitgliedern vorhanden sind, die sich im Besitz von TAPI befinden. Die Beschreibung, welche Member vom Dienstanbieter festgelegt und welche beibehalten werden müssen, finden Sie im Abschnitt Funktionen der Funktionen, die auf diese Datenstruktur verweisen.

Für jede Struktur werden im Referenzabschnitt die folgenden Elemente aufgeführt:

-   Der Zweck der -Struktur
-   Eine Beschreibung der Werte oder Felder
-   Eine Beschreibung der Erweiterbarkeit der Struktur
-   Optionale Kommentare zur Verwendung der -Struktur
-   Optionale Verweise auf andere Funktionen, Meldungen, Konstanten oder Strukturen.

Arbeitsspeicher für alle Datenstrukturen, deren Darstellung sowohl von TAPI als auch vom Dienstanbieter veröffentlicht und gemeinsam genutzt wird, wird über TAPI oder eine Anwendung mit TAPI zugeordnet. TAPI übergibt einen Zeiger auf die TSPI-Funktion, die die Informationen zurückgibt. TSPI füllt die Datenstruktur mit den angeforderten Informationen auf. Wenn der Vorgang asynchron ist, sind die Informationen erst verfügbar, wenn der asynchrone Antwortrückruf einen Erfolg anzeigt.

> [!Note]  
> Einige Strukturen enthalten Felder für Größe und Offset zum Definieren der Position und Länge von Zeichenfolgen im Variablenteil der Struktur. Wenn der Dienstanbieter aufgefordert wird, eine Zeichenfolge hinzuzufügen, aber keine Zeichenfolge verfügbar ist, muss der Dienstanbieter diese Bedingung auf eine der folgenden Arten angeben:
>
> -   Legen Sie die Felder Größe und Offset auf 0 fest.
> -   Legen Sie das Feld Offset auf ungleich null, aber Auf Größe auf 0 fest.
> -   Legen Sie das Feld Offset auf ungleich null, Size auf 1 und das Byte am Offset auf 0 fest.

 

 

 
