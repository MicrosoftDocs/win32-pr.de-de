---
description: In einer relationalen Datenbank müssen Zeilen, die von einer Suchabfrage zurückgegeben werden, alle von der Abfrage aufgerufenen Bedingungen erfüllen. Im Gegensatz dazu kann eine Windows Search-Abfrage Dokumente zurückgeben, die die Suchbedingungen in unterschiedlichem Maße erfüllen.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Grundlegendes zu Relevanzwerten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d28efba26d12e0260d76e02fc4e042e72612df34d383a0e22a34f4be9d9fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226805"
---
# <a name="understanding-relevance-values"></a>Grundlegendes zu Relevanzwerten

In einer relationalen Datenbank müssen Zeilen, die von einer Suchabfrage zurückgegeben werden, alle von der Abfrage aufgerufenen Bedingungen erfüllen. Im Gegensatz dazu kann eine Windows Search-Abfrage Dokumente zurückgeben, die die Suchbedingungen in unterschiedlichem Maße erfüllen.

Beispielsweise erzeugt eine Suche nach dem Begriff "Program" in einer relationalen Datenbank Datensätze, die diese spezifische Schreibweise des Worts enthalten. Ob ein Datensatz eine oder 100 Instanzen des Worts enthält, hat keine Auswirkungen auf die Ergebnisse. Im Gegensatz dazu gibt Windows Search einen Relevanzwert zurück, der den übereinstimmenden Dokumenten zugeordnet ist. Die Relevanz von Dokumenten mit "Program" im Titel ist höher als diejenigen, die das Wort nur im letzten Absatz enthalten. Ebenso stimmen Dokumente, die Variationen des Suchbegriffs enthalten, z. B. "Programme" und "Programmierung", ebenfalls überein und werden von der Abfrage zurückgegeben.

Windows Suchabfragen geben ganzzahlige Relevanzwerte in der Spalte mit dem Namen "rank" zurück.

Zusätzlich:

-   Von der Abfrage zurückgegebene Rangwerte sind ganze Zahlen im Bereich von 0 bis 1000.
-   Höhere Rangwerte geben Dokumente an, die den Suchbedingungen besser entsprechen.
-   Rangwerte gelten nur für die aktuelle Abfrage, sodass sie nicht abfrageübergreifend mit Ergebnissen verglichen werden können.
-   Rangwerte sind relativ zu den anderen Dokumenten, die mit der Abfrage übereinstimmen. Daher hängt der Rangwert eines bestimmten Dokuments von den anderen Dokumenten ab, die auch mit der Abfrage übereinstimmen.
-   Rangwerte für Elemente, die einem rein relationalen Prädikat entsprechen, sind 1000.

Sie können die zurückgegebenen Rangwerte bearbeiten, indem Sie Spaltengewichtungen in den Prädikaten der [CONTAINS-](-search-sql-contains.md) und [FREETEXT](-search-sql-freetext.md) WHERE-Klausel und der RANK BY-Klausel verwenden.

 

 



