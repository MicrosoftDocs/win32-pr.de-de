---
description: In einer relationalen Datenbank müssen Zeilen, die von einer Suchabfrage zurückgegeben werden, alle Bedingungen erfüllen, die von der Abfrage aufgerufen werden. Im Gegensatz dazu kann eine Windows Search-Abfrage Dokumente zurückgeben, die die Suchbedingungen in variierender Grad erfüllen.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Verstehen von relevanzwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862151"
---
# <a name="understanding-relevance-values"></a>Verstehen von relevanzwerten

In einer relationalen Datenbank müssen Zeilen, die von einer Suchabfrage zurückgegeben werden, alle Bedingungen erfüllen, die von der Abfrage aufgerufen werden. Im Gegensatz dazu kann eine Windows Search-Abfrage Dokumente zurückgeben, die die Suchbedingungen in variierender Grad erfüllen.

Eine Suche nach dem Begriff "Program" in einer relationalen Datenbank erzeugt z. b. Datensätze, die die jeweilige Schreibweise des Worts enthalten. Ob ein Datensatz eine oder 100 Instanzen des Worts enthält, hat keine Auswirkung auf die Ergebnisse. Im Gegensatz dazu gibt Windows Search einen relevanzwert zurück, der mit den übereinstimmenden Dokumenten verknüpft ist. Die Relevanz von Dokumenten mit dem Titel "Program" im Titel ist höher als diejenigen, die das Wort nur im letzten Absatz enthalten. Ebenso Stimmen Dokumente, die Variationen des Suchbegriffs enthalten, z. b. "Programme" und "Programming", auch mit der Abfrage zurück.

Windows Search-Abfragen geben ganzzahlige Relevanzwerte in der Spalte mit dem Namen "Rank" zurück.

Zusätzlich:

-   Von der Abfrage zurückgegebene Rang Werte sind ganze Zahlen zwischen 0 und 1000.
-   Höhere Rang Werte geben Dokumente an, die den Suchbedingungen besser entsprechen.
-   Rang Werte gelten nur für die aktuelle Abfrage und können daher nicht für Abfragen über Abfragen hinweg verglichen werden.
-   Rang Werte sind relativ zu den anderen Dokumenten, die mit der Abfrage übereinstimmen. Der Rangwert eines bestimmten Dokuments hängt daher von den anderen Dokumenten ab, die ebenfalls der Abfrage entsprechen.
-   Rang Werte für Elemente, die mit einem rein relationalen Prädikat übereinstimmen, sind 1000.

Sie können die zurückgegebenen Rang Werte mithilfe von Spalten Gewichtungen in den WHERE-Klausel-Prädikaten " [enthält](-search-sql-contains.md) " und " [fretext](-search-sql-freetext.md) " und der Rang-nach-Klausel bearbeiten.

 

 



