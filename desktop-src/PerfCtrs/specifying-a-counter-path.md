---
description: Das System verwendet Leistungsindikatoren, um Leistungsdaten zu sammeln.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Angeben eines Indikatorpfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a359762e4d959992bebd338c4b3ee29825c63b4cb081b70722c82fb3376b5d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143803"
---
# <a name="specifying-a-counter-path"></a>Angeben eines Indikatorpfads

Das System verwendet Leistungsindikatoren, um Leistungsdaten zu sammeln. Jeder Leistungsindikator wird durch seinen Namen und seinen Pfad oder Speicherort eindeutig identifiziert. Die Syntax eines Indikatorpfads lautet:

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

Das Computer -Element gibt den Namen oder die IP-Adresse des Computers an, von dem aus Sie Leistungsdaten abfragen möchten. Der Computername ist optional, wenn sich der Leistungsindikator auf dem lokalen Computer befindet.

Das PerfObject-Element gibt das abzufragende Leistungsobjekt an. Ein Leistungsobjekt kann eine physische Komponente wie Prozessoren, Datenträger und Arbeitsspeicher oder ein Systemobjekt wie Prozesse und Threads sein. Jedes Systemobjekt ist mit einem funktionalen Element innerhalb des Computers verknüpft und verfügt über eine Reihe von Standardindikatoren, die ihm zugewiesen sind. Auf jedem Computer kann ein anderer Satz von Leistungsobjekten und Leistungsindikatoren installiert sein, da Anwendungen ihre eigenen Leistungsobjekte und Leistungsindikatoren installieren können. Eine Liste der Leistungsobjekte und Leistungsindikatoren, die auf Ihrem Computer installiert sind, finden Sie im Dialogfeld **Leistungsindikatoren hinzufügen** im Leistungstool auf Ihrem Computer. Diese Objekte werden auch im Dialogfeld PDH-Durchsuchen aufgeführt (siehe [Durchsuchen von Indikatoren).](browsing-counters.md) Eine Liste der Systemleistungsobjekte und -indikatoren finden Sie unter [Leistungsindikatoren nach Objekt.](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10))

ParentInstance, ObjectInstance und InstanceIndex sind im Pfad enthalten, wenn mehrere Instanzen des Objekts vorhanden sein können. Prozesse und Threads sind beispielsweise mehrere Instanzobjekte, da mehrere Prozesse oder Threads gleichzeitig ausgeführt werden können. Wenn ein Objekt über mehrere Instanzen verfügen kann, muss der Indikatorpfad eine Objektinstanz angeben.

Das Format der instanzbezogenen Elemente hängt vom Objekttyp ab. Wenn das Objekt über einfache Instanzen verfügt, ist das Format nur der Instanzname, der in Klammern eingeschlossen ist. Beispiel:

``` syntax
(Explorer)
```

Wenn für die Instanz dieses Objekts auch ein übergeordneter Instanzname erforderlich ist, muss der Name der übergeordneten Instanz vor der Objektinstanz stehen und durch einen Schrägstrich getrennt werden. Beispielsweise gehören Threads zu Prozessen. Wenn Sie ein Threadobjekt abfragen, müssen Sie auch den Prozess angeben, zu dem es gehört, wie im folgenden Beispiel gezeigt:

``` syntax
(Explorer/0)
```

Wenn das Objekt über mehrere Instanzen mit der gleichen Namenszeichenfolge verfügt, können sie sequenziell indiziert werden, indem sie den Instanzindex angeben, dem ein Nummernzeichen vorangestellt ist. Instanzindizes sind 0-basiert. Wenn Sie die erste Instanz abfragen möchten, schließen Sie nicht 0 ein, \# sondern geben Sie einfach den Instanznamen an. Um die zweite Instanz anzugeben, verwenden Sie \# 1, um die dritte Instanz anzugeben, \# verwenden Sie 2 usw. Beispiel:

``` syntax
(Explorer/0#1)
```

Das Counter-Element gibt den Leistungsindikator an, den Sie für das angegebene Leistungsobjekt abfragen möchten.

PDH verwendet die folgenden Sonderzeichen in einem Indikatorpfad. Anbieter sollten diese Zeichen nicht in ihren Namen verwenden. Wenn ein Anbieter diese Sonderzeichen verwendet, kann PDH den vollständigen Indikatorpfad nicht analysieren, um die Indikator- und Instanznamen abzurufen.



| Zeichen | BESCHREIBUNG                                                |
|-----------|------------------------------------------------------------|
| \\        | Generisches Trennzeichen für Computer, Objekt und Indikator.       |
| (         | Anfang des Instanznamens.                                |
| )         | Ende des Instanznamens.                                   |
| /         | Trennt die Instanz und die übergeordnete Instanz.                    |
| \#n       | Identifiziert ein bestimmtes Vorkommen einer instanz mit dem gleichen Namen. |
| \*        | Platzhalterzeichen.                                        |



 

Die folgenden Beispiele zeigen die möglichen Formate für Indikatorpfade:

-   \\\\\\Computerobjektzähler (übergeordneter \# Index/Instanzindex) \\
-   \\\\computer \\ object(parent/instance) \\ counter
-   \\\\\\Computerobjektzähler \# (Instanzindex) \\
-   \\\\\\Computerobjektzähler (Instanz) \\
-   \\\\\\ \\ Computerobjektzähler
-   \\object(parent/instance \# index) \\ counter
-   \\object(parent/instance) \\ counter
-   \\object(instance \# index) \\ counter
-   \\\\object(instance)-Indikator
-   \\\\Objektzähler

## <a name="using-wildcard-characters"></a>Verwenden von Platzhalterzeichen

Indikatorpfade dürfen ein Platzhalterzeichen nur für den Instanznamen enthalten, wie im folgenden Beispiel gezeigt.

``` syntax
\Process(*)\% Processor Time
```

Um den Platzhalter in eine Liste von Indikatorpfaden zu erweitern, die Instanzen enthalten, die auf dem Computer oder in der Protokolldatei gefunden wurden, rufen Sie [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha)auf.

 

 
