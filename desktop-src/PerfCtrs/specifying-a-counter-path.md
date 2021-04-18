---
description: Das System verwendet Leistungsindikatoren, um Leistungsdaten zu erfassen.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Angeben eines Indikatorpfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3a92f94b4bf3d2252903d92785f43bb0cac110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347362"
---
# <a name="specifying-a-counter-path"></a>Angeben eines Indikatorpfads

Das System verwendet Leistungsindikatoren, um Leistungsdaten zu erfassen. Jeder Counter wird durch seinen Namen und Pfad bzw. Speicherort eindeutig identifiziert. Die Syntax eines Counter-Pfads lautet wie folgt:

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

Das Computer Element gibt den Namen oder die IP-Adresse des Computers an, von dem Sie die Leistungsdaten Abfragen möchten. Der Computername ist optional, wenn sich der gegen Computer auf dem lokalen Computer befindet.

Das perfobject-Element gibt das abzufragende Leistungs Objekt an. Ein Leistungs Objekt kann eine physische Komponente sein, z. b. Prozessoren, Datenträger und Arbeitsspeicher, oder ein Systemobjekt, z. b. Prozesse und Threads. Jedes Systemobjekt ist mit einem funktionalen Element innerhalb des Computers verknüpft und verfügt über einen Satz von Standard Zählern. Auf jedem Computer sind möglicherweise andere Leistungs Objekte und Leistungsindikatoren installiert, da Anwendungen eigene Leistungs Objekte und-Indikatoren installieren können. Eine Liste der Leistungs Objekte und-Indikatoren, die auf Ihrem Computer installiert sind, finden Sie im Dialogfeld Leistungsindikatoren **Hinzufügen** im Leistungs Tool auf dem Computer. Diese Objekte werden auch im Dialogfeld PDH-durchsuchen aufgelistet (siehe Such [Zähler](browsing-counters.md)). Eine Liste der Systemleistungs Objekte und-Indikatoren finden Sie unter Indikatoren [nach Objekt](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).

Die Parametern instance, ObjectInstance und instanceindex sind im Pfad enthalten, wenn mehrere Instanzen des Objekts vorhanden sein können. Prozesse und Threads sind z. b. mehrere Instanzobjekte, da mehrere Prozesse oder Threads gleichzeitig ausgeführt werden können. Wenn ein Objekt über mehr als eine Instanz verfügen kann, muss der Counter-Pfad eine Objektinstanz angeben.

Das Format der instanzbezogenen Elemente hängt vom Objekttyp ab. Wenn das-Objekt über einfache Instanzen verfügt, ist das Format nur der in Klammern eingeschlossene Instanzname. Beispiel:

``` syntax
(Explorer)
```

Wenn für die Instanz dieses Objekts auch ein übergeordneter Instanzname erforderlich ist, muss der Name der übergeordneten Instanz vor der Objektinstanz stehen und durch einen Schrägstrich getrennt werden. Threads gehören z. b. zu Prozessen. Wenn Sie ein Thread Objekt Abfragen, müssen Sie auch den Prozess angeben, zu dem er gehört, wie im folgenden Beispiel gezeigt:

``` syntax
(Explorer/0)
```

Wenn das Objekt mehrere Instanzen mit derselben namens Zeichenfolge aufweist, können diese sequenziell indiziert werden, indem der Instanzindex angegeben wird, dem ein Nummern Zeichen vorangestellt ist. Instanzindizes sind 0-basiert. Wenn Sie die erste Instanz abfragen möchten, schließen Sie 0 nicht ein \# – Geben Sie einfach den Instanznamen an. Um die zweite Instanz anzugeben, verwenden \# Sie 1. um die dritte Instanz anzugeben, verwenden Sie \# 2 usw. Beispiel:

``` syntax
(Explorer/0#1)
```

Das Counter-Element gibt den Leistungs Zählers an, den Sie für das angegebene Leistungs Objekt Abfragen möchten.

PDH verwendet die folgenden Sonderzeichen in einem Counter-Pfad. Anbieter sollten diese Zeichen nicht in ihren Namen verwenden. Wenn ein Anbieter diese Sonderzeichen verwendet, kann PDH den vollständigen Counter-Pfad nicht analysieren, um den Namen des Zählers und der Instanzen abzurufen.



| Zeichen | BESCHREIBUNG                                                |
|-----------|------------------------------------------------------------|
| \\        | Allgemeines Trennzeichen für Computer, Objekt und Counter.       |
| (         | Anfang des Instanznamens.                                |
| )         | Das Beenden des Instanznamens.                                   |
| /         | Trennt die Instanz und die übergeordnete Instanz.                    |
| \#n       | Identifiziert ein bestimmtes Vorkommen einer Instanz mit demselben Namen. |
| \*        | Platzhalter Zeichen.                                        |



 

In den folgenden Beispielen werden die möglichen Formate für-Counter-Pfade veranschaulicht:

-   \\\\Computer \\ Objekt (übergeordneter/ \# Instanzindex) Indikator \\
-   \\\\Computer \\ Objekt (über-/Instanz-Counter) \\
-   \\\\Indikator für Computer \\ Objekt (Instanzindex \# ) \\
-   \\\\Computer \\ Objekt (Instanz)- \\ Counter
-   \\\\Computer \\ Objekt- \\ Counter
-   \\Objekt Indikator (übergeordneter/ \# Instanzindex) \\
-   \\Objekttyp (übergeordnet/ \\ Instanz)
-   \\Indikator für Objekt ( \# Instanzindex) \\
-   \\Objekt-(Instanz-) \\ Counter
-   \\Objekt- \\ Counter

## <a name="using-wildcard-characters"></a>Verwenden von Platzhalter Zeichen

Die Anzahl der Pfade kann ein Platzhalter Zeichen nur für den Instanznamen enthalten, wie im folgenden Beispiel gezeigt.

``` syntax
\Process(*)\% Processor Time
```

Um das Platzhalter Zeichen in eine Liste von Counter-Pfaden zu erweitern, die auf dem Computer oder in der Protokolldatei gefundene Instanzen enthalten, nennen Sie [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).

 

 
