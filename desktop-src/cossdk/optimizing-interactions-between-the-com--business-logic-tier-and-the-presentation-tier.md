---
description: In der Regel unterscheidet sich die Latenz zwischen den Ebenen einer verteilten Anwendung erheblich.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Optimieren von Interaktionen zwischen der COM+-Geschäftslogikebene und der Präsentationsebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca519c6aa7f1585648b0def6530b7f224f12a98961193e4f6f7cc490a747b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306102"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Optimieren von Interaktionen zwischen der COM+-Geschäftslogikebene und der Präsentationsebene

In der Regel unterscheidet sich die Latenz zwischen den Ebenen einer verteilten Anwendung erheblich. Aufrufe zwischen der Präsentationsebene und der Geschäftslogikebene sind häufig um ein Vielfaches langsamer als Aufrufe zwischen der Geschäftsebene und der Datenschicht. Daher ist der Zustand "Held" teurer, wenn die Geschäftslogikebene aufgerufen wird.

In den folgenden Themen werden Möglichkeiten zum Übergeben von Daten zwischen präsentations- und geschäftslogikebenen erörtert:

-   [Übergeben von Parametern](#passing-parameters)
-   [Datenübergabeoptionen](#data-passing-options)
-   [Verwenden eines Factorymusters zum Übergeben von Daten](#using-a-factory-pattern-to-pass-data)
-   [Zugehörige Themen](#related-topics)

## <a name="passing-parameters"></a>Übergeben von Parametern

Damit ein bestimmter Satz von Informationen zwischen der Präsentationsebene und der Geschäftslogikebene übergeben wird, verfügen Sie möglicherweise über eine einzelne Zeile, mehrere Zeilen oder eine Kombination aus einer einzelnen Zeile (z. B. einem Header) und mehreren Detailzeilen von Daten. Die effizienteste Möglichkeit, diese Informationen zwischen Ebenen zu übergeben, ist ein einzelner Methodenaufruf. Mit diesem einzelnen Aufruf wird der gesamte zu übergebende Informationssatz verwaltet. Dies ist erforderlich, es sei denn, Sie entscheiden sich dafür, die Transaktion von der Präsentationsebene aus zu steuern (und alle Transaktionsbehandlungen auf der Präsentationsebene in der Funktion identisch zu machen). Microsoft empfiehlt nicht, Transaktionen von der Präsentationsebene aus durchzuführen, da Aufrufe zwischen dieser Ebene und der Geschäftslogikebene in der Regel die langsamsten Aufrufe in einer Anwendung mit mehreren Ebenen sind.

Eine Möglichkeit zum Erstellen einer solchen Methode besteht darin, einzelne Informationszeilen als Parameter und mehrere Zeilen als ADO-Recordsets zu übergeben. Recordsets sind der Kern der ADO-Datenzugriffsmethodik von Microsoft, und die Verwendung von ADO-Recordsets ermöglicht es Ihnen, alle Informationen im Zusammenhang mit einer einzelnen Transaktion in einem Schritt zu übergeben.

## <a name="data-passing-options"></a>Datenübergabeoptionen

Es gibt weitere Optionen, die beim Übergeben von Daten zu berücksichtigen sind. Dazu gehören die Verwendung einer Liste von Parametern und ADO-Recordsets (wie oben beschrieben), nur ADO-Recordsets, XML-codierte Zeichenfolgen oder Arrays von Strukturen. In diesem Abschnitt wird jede dieser Optionen erläutert.

Die folgende Tabelle zeigt Bereiche, in denen bei der Verwendung einer der vier verschiedenen Argumentübergabemöglichkeiten besondere Vorsicht walten muss. Ein "X" stellt Bereiche dar, in denen Vor- und Vorzeichen verstanden und gegen die Anforderungen der einzelnen Projekte abgewogen werden müssen. Versuchen Sie nicht, Argumentübergabeentscheidungen auf Komponentenbasis zu treffen. Die Vorteile eines konsistenten Programmiermodells in einem Projekt überwiegen bei weitem jeden Vorteil der Optimierung pro Methode oder pro Komponente in allen, aber extremsten Umständen. Die Spalten werden in der Liste beschrieben, die auf die Tabelle folgt.



|     &nbsp;                  | Parallelität  | WAN          | Bereitstellung   | Komplexität   |
|-----------------------|--------------|--------------|--------------|--------------|
| Eingabe | Wert |
| Recordsets<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Arrays<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Die vier Spalten definieren Bereiche, auf die sie achten sollten, wenn sie diese Option zum Übergeben von Parametern verwenden.

-   **Die Spalte Concurrency** stellt die Notwendigkeit dar, einen Mechanismus zu codieren oder bereitzustellen, der Sperrbedingungen für Updatevorgänge verwaltet. Da Methoden, die Einsparungen ausführen, Updates darstellen können, können Parallelitätsprobleme auftreten. Zwei Arten von Sperren sind weit verbreitet optimistisch und pessimistisch. Pessimistische Sperren verhindern, dass ein Benutzer Daten für das Update erhält, während ein anderer Benutzer das Potenzial hat, ein Update durchzuführen. Die optimistische Sperre unterstützt sehr viele weitere Benutzer, indem sie mit der Wahrscheinlichkeit abgerechnet wird, dass zwei Benutzer dasselbe Dokument gleichzeitig aktualisieren. Optimistische Sperren rufen zur Überprüfung auf, ob die gespeicherten Daten mit den Daten übereinstimmen, zu dem Zeitpunkt, zu dem auf eine Kopie der Daten zur Änderung zugegriffen wurde. ADO-Recordsets bieten automatische Unterstützung für optimistische Sperren. Updateszenarien, die Einzelne-Zeilen-Parameterlisten enthalten, bieten keine ausreichende Unterstützung für die Parallelitätsprüfung. XML unterliegt diesem Problem, da in XML-Daten keine Sperrinformationen vorhanden sind.
-   **Die WAN-Spalte** stellt Bedingungen dar, bei denen es in einem Wan (Wide Area Network) zu Übertragungsinhalten kommen kann. Wenn das WAN nicht über genügend Kapazität zum Verwalten aller Daten verfügt, die gleichzeitig verschoben werden, kommt es bei Anwendungsbenutzern zu Verzögerungen bei der Antwortzeit. Um optimistische Parallelität zu unterstützen, übergeben getrennte ADO-Recordsets zwei Kopien der Daten vom Server an den Client. Die zweite Kopie wird vom Client verwendet, um das kleinste Updaterowset zu bestimmen, das beim Commit einer Änderung übergeben werden soll. Dies reduziert zwar den Datenverkehr von der Präsentationsebene zu den Daten, aber die zusätzliche Last der zweiten Kopie kann erheblich sein. Die Verwendung von Recordsets als einziges Mittel zum Übergeben aller Informationen führt daher dazu, dass doppelt so viele Daten zwischen Ebenen wie erforderlich übergeben werden, es sei denn, das Updaterowset wird von einer Präsentationsebene zurück an die Datenebene übergeben.
-   **Die Spalte Bereitstellung** stellt Probleme im Zusammenhang mit der Datenübergabe dar, wenn sowohl auf der Aufrufer- als auch auf der Komponentenseite des Netzwerks eine spezielle Technologie erforderlich ist. Die Verwendung von ADO-Recordsets erfordert beispielsweise, dass ADO-Komponenten sowohl auf dem Client als auch auf dem Server vorhanden sind. XML-Parser müssen auch auf beiden Seiten vorhanden sein, um zu vermeiden, dass Parser in Ihre Anwendungen codiert werden müssen.
-   **Die Spalte Komplexität** ist für alle vier Optionen angegeben und ist eine Frage der Präferenz oder vorherigen Programmiermodellerfahrung, die möglicherweise bereits in Ihrer Entwicklungsorganisation eingerichtet wurde. Einige Benutzer finden die Übergabe von Parametern umständlich und haben das Gefühl, dass dies dem Programmierproblem zu viel Komplexität hinzufügt. Wenn Sie nachverfolgen, welchen Parameter Sie behandeln, und sie alle in einem Bearbeitungsfenster sichtbar machen, kann dies zu einer erhöhten Komplexität führen, die von einigen Entwicklern als nicht verwaltet bezeichnet wird.

Die Parameterübergabemethode kann auch Vor- und Nachholungen aufweisen, z. B. die folgenden:

-   Parameter können die Verwaltung mehrerer Argumente und Argumenttypen sowie die Entscheidung umfassen, wann ein Recordset als Parameter geeignet ist.
-   ADO-Recordsets können hierarchische Beziehungen in Methodenparametern auf ein oder zwei Argumente reduzieren. Dies vereinfacht das Programmiermodell erheblich und unterstützt das Hinzufügen von Spalten zu einem späteren Zeitpunkt, blendet aber auch die Informationshierarchie aus. Das Zusammenfüllen von Informationen in ein ADO-Recordset und das spätere Extrahieren umfassen das Kennen der Namen der einzelnen Spalten oder die Kenntnis der Spaltenreihenfolge. Diese Situation kann die Komplexität für andere Komponenten- oder Anwendungsentwickler im Projekt erhöhen.
-   XML ist ein anderer Drehung der oben erwähnten verborgenen Hierarchiekomplizierung. Der Programmierer muss die Verwendung eines XML-Parsers verstehen, um Zugriff auf die Informationen zu erhalten, und häufig die Namen der einzelnen Elemente im DataSet kennen, bevor das Dataset gefunden werden kann.
-   Arrays von Strukturen führen dazu, dass ein gemeinsames Verständnis der Informationen erforderlich ist, die sowohl vom Aufrufer als auch von der Komponente übergeben werden. Diese Notwendigkeit einer Zuordnung, die von zwei Systemelementen gemeinsam genutzt wird, kann zu Schwierigkeiten beim Umgang mit verschiedenen Versionen von Komponenten führen. Obwohl sich die Methodensignatur möglicherweise nicht ändert, können Änderungen an den erwarteten Informationen aufrufende Programme inkompatibel machen.

Da die Komplexitätsprobleme, die mit allen vier Parameterübergabemethoden verbunden sind, so ähnlich sind, ist es nicht zu diskutieren, dass eine erhebliche Vereinfachungsmöglichkeit mit einer auswahl verbunden ist.

## <a name="using-a-factory-pattern-to-pass-data"></a>Verwenden eines Factorymusters zum Übergeben von Daten

Ein wichtiger Entwurfspunkt ist die Benutzerfreundlichkeit. Als Sie sich entschieden haben, ADO-Recordsets zu verwenden, um einen strukturierten Satz von Details zurück an die Präsentationsebene zu übergeben, haben Sie ein Komplexitätsproblem eingeführt. Programmierer der Präsentationsebene müssen die Struktur dieser Recordsets verstehen. Ein komplexeres Problem kann auftreten, wenn Sie mehrere Details benötigen, damit ein Satz von Daten in einem Recordset übergeben wird. Zur Vereinfachung sollten Sie immer dann eine Recordsetfactorymethode erstellen, wenn Sie möchten, dass Daten in strukturierten ADO-Recordsets übergeben werden.

Die Recordsetfactory sollte ein leeres, aber beschreibbares getrenntes Recordset an den Aufrufer zurückgeben. Dieses Recordset sollte die richtigen Felder (Namen und Datentypen) bereits konfiguriert haben, damit der aufrufende Client nicht wissen muss, wie das Recordset hergestellt werden soll. Dieser Ansatz wird häufig als *Factorymuster* bezeichnet und ist ein gängiges Lösungsmuster, das die Notwendigkeit löst, ein Objekt mit einer bestimmten Komplexität zu erstellen, ohne die Nuancen der Erstellung kennen zu müssen.

Einfache Entwurfsentscheidungen, z. B. das Auswählen des gleichen Parameternamens für denselben Datenteil für jede Methode, bei der diese Informationen übergeben werden, erleichtern es, eine Methode zu betrachten und zu wissen, was erwartet wird. Die Sicherstellung, dass die Reihenfolge, in der like-Argumente übergeben werden, über eine gesamte Methodenfamilie hinweg konsistent ist, stellt einen Komfortpunkt dar, der ein konsistentes Modell erzwingt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Optimieren von Interaktionen zwischen der COM+-Geschäftslogikebene und der Datenschicht](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




