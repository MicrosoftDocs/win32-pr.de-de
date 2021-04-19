---
description: Die von TSPI verwendeten Datenstrukturen sind identisch mit denen, die in TAPI-Strukturen definiert sind, mit Ausnahme von "tuispikreatedialoginstancepara".
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: TSPI-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348600"
---
# <a name="tspi-structures"></a>TSPI-Strukturen

Die von TSPI verwendeten Datenstrukturen sind identisch mit denen, die in [TAPI-Strukturen](./tapi-structures.md)definiert sind, mit Ausnahme von " [**tuispikreatedialoginstancepara**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)".

Bei den meisten größeren Datenstrukturen ist die Verantwortung für das Ausfüllen von Membern zwischen dem Dienstanbieter und TAPI aufgeteilt. Der Dienstanbieter muss die Werte, die in Membern von TAPI vorhanden sind, beibehalten. Die Beschreibung, welche Member vom Dienstanbieter festgelegt werden müssen und welche beibehalten werden muss, wird im Abschnitt Functions in den Funktionen bereitgestellt, die auf diese Datenstruktur verweisen.

Der Abschnitt Reference listet für jede Struktur die folgenden Elemente auf:

-   Der Zweck der Struktur
-   Eine Beschreibung der Werte oder Felder.
-   Eine Beschreibung der Erweiterbarkeit der Struktur.
-   Optionale Kommentare zur Verwendung der Struktur
-   Optionale Verweise auf andere Funktionen, Nachrichten, Konstanten oder Strukturen.

Der Arbeitsspeicher für alle Datenstrukturen, deren Darstellung sowohl von TAPI als auch vom Dienstanbieter veröffentlicht und freigegeben wird, wird von TAPI oder einer Anwendung mithilfe von TAPI zugeordnet. TAPI übergibt einen Zeiger an die TSPI-Funktion, die die Informationen zurückgibt. TSPI füllt die Datenstruktur mit den angeforderten Informationen. Wenn der Vorgang asynchron ist, sind die Informationen erst verfügbar, wenn der asynchrone Antwort Rückruf einen Erfolg angibt.

> [!Note]  
> Einige Strukturen enthalten Größen-und Offset Felder zum Definieren der Position und Länge von Zeichen folgen im Variablen Teil der Struktur. Wenn der Dienstanbieter aufgefordert wird, eine Zeichenfolge hinzuzufügen, aber keine Zeichenfolge verfügbar ist, muss der Dienstanbieter diese Bedingung auf eine der folgenden Weisen angeben:
>
> -   Legen Sie die Felder Größe und Offset auf 0 fest.
> -   Legen Sie für das Offset-Feld einen Wert ungleich 0 (null) fest.
> -   Legen Sie für das Offset-Feld den Wert ungleich 0 (null), für Größe 1 und für das Byte am Offset den Wert 0 fest.

 

 

 
