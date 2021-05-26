---
description: In der Regel unterscheidet sich die Latenz zwischen den Ebenen einer verteilten Anwendung erheblich.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Optimieren von Interaktionen zwischen der COM+-Geschäftslogikebene und der Präsentationsebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3258453a16549eacf3a7ed77444674d425c85613
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423500"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Optimieren von Interaktionen zwischen der COM+-Geschäftslogikebene und der Präsentationsebene

In der Regel unterscheidet sich die Latenz zwischen den Ebenen einer verteilten Anwendung erheblich. Aufrufe zwischen der Präsentationsebene und der Geschäftslogikebene sind häufig um ein Vielfaches langsamer als Aufrufe zwischen der Geschäftsebene und der Datenschicht. Daher ist der Zustand "Held" teurer, wenn die Geschäftslogikebene aufgerufen wird.

In den folgenden Themen werden Möglichkeiten zum Übergeben von Daten zwischen präsentations- und geschäftslogikebenen erörtert:

-   [Übergeben von Parametern](#passing-parameters)
-   [Datenübergabeoptionen](#data-passing-options)
-   [Verwenden eines Factorymusters zum Übergeben von Daten](#using-a-factory-pattern-to-pass-data)
-   [Verwandte Themen](#related-topics)

## <a name="passing-parameters"></a>Übergeben von Parametern

Damit ein bestimmter Satz von Informationen zwischen der Präsentationsebene und der Geschäftslogikebene übergeben wird, verfügen Sie möglicherweise über eine einzelne Zeile, mehrere Zeilen oder eine Kombination aus einer einzelnen Zeile (z. B. einem Header) und mehreren Detailzeilen von Daten. Die effizienteste Möglichkeit, diese Informationen zwischen Ebenen zu übergeben, ist ein einzelner Methodenaufruf. Mit diesem einzelnen Aufruf wird der gesamte zu übergebende Informationssatz verwaltet. Dies ist erforderlich, es sei denn, Sie entscheiden sich dafür, die Transaktion von der Präsentationsebene aus zu steuern (und alle Transaktionsbehandlungen auf der Präsentationsebene in der Funktion identisch zu machen). Microsoft empfiehlt nicht, Transaktionen von der Präsentationsebene aus durchzuführen, da Aufrufe zwischen dieser Ebene und der Geschäftslogikebene in der Regel die langsamsten Aufrufe in einer Anwendung mit mehreren Ebenen sind.

Eine Möglichkeit zum Erstellen einer solchen Methode besteht darin, einzelne Informationszeilen als Parameter und mehrere Zeilen als ADO-Recordsets zu übergeben. Recordsets sind der Kern der ADO-Datenzugriffsmethodik von Microsoft, und die Verwendung von ADO-Recordsets ermöglicht es Ihnen, alle Informationen im Zusammenhang mit einer einzelnen Transaktion in einem Schritt zu übergeben.

## <a name="data-passing-options"></a>Datenübergabeoptionen

Es gibt weitere Optionen, die beim Übergeben von Daten zu berücksichtigen sind. Dazu gehören die Verwendung einer Liste von Parametern und ADO-Recordsets (wie oben beschrieben), nur ADO-Recordsets, XML-codierte Zeichenfolgen oder Arrays von Strukturen. In diesem Abschnitt werden die einzelnen Optionen erläutert.

In der folgenden Tabelle sind Bereiche aufgeführt, in denen bei verwendung einer der vier verschiedenen Argumentübergebungsmöglichkeiten besondere Vorsicht zu bieten ist. Ein "X" stellt Bereiche dar, in denen Vor- und Abwägungen verstanden und gegen die Anforderungen der einzelnen Projekte abgewogen werden müssen. Versuchen Sie, keine Entscheidungen über die Argumentübergeteilung auf Komponentenbasis zu treffen. Die Vorteile eines konsistenten Programmiermodells in einem Projekt übersteigt bei allen bis auf die extremsten Umstände den Vorteil einer Methoden- oder Komponentenoptimierung. Die Spalten werden in der Liste beschrieben, die auf die Tabelle folgt.



|     &nbsp;                  | Parallelität  | WAN          | Bereitstellung   | Komplexität   |
|-----------------------|--------------|--------------|--------------|--------------|
| Eingabe | Wert |
| Recordsets<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Arrays<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Die vier Spalten definieren Bereiche, auf die Sie achten müssen, wenn Sie diese Option zum Übergeben von Parametern verwenden.

-   **Die Spalte Parallelität stellt** die Notwendigkeit dar, einen Mechanismus zum Verwalten von Sperrbedingungen für Updatevorgänge zu codieren oder bereitstellen. Da Methoden, die Speichern ausführen, Updates darstellen können, können Parallelitätsprobleme auftreten. Zwei Arten von Sperren sind häufig optimistisch und pessimistisch. Pessimistische Sperren verhindern, dass ein Benutzer Daten zum Aktualisieren abrufen kann, während ein anderer Benutzer das Potenzial hat, ein Update zu durchführen. Die optimistische Sperre unterstützt deutlich mehr Benutzer, indem gegen die Wahrscheinlichkeit gehandelt wird, dass zwei Benutzer dasselbe Dokument gleichzeitig aktualisieren würden. Die optimistische Sperrung erfordert die Überprüfung, um zu überprüfen, ob die gespeicherten Daten den Daten zu dem Zeitpunkt entspricht, an dem zur Änderung auf eine Kopie der Daten zugegriffen wurde. ADO-Recordsets bieten automatische Unterstützung für optimistische Sperren. Updateszenarien, die Einzelne-Zeilen-Parameterlisten enthalten, bieten keine ausreichende Unterstützung für die Parallelitätsüberprüfung. XML hat das gleiche Problem, da in XML-Daten kein Sperrbewusstsein vorhanden ist.
-   **Die WAN-Spalte** stellt Bedingungen dar, unter denen Übertragungsübertritte in einem Wan (Wide Area Network) möglich sind. Wenn das WAN nicht über genügend Kapazität verfügt, um alle zu verschiebenden Daten gleichzeitig zu verwalten, kommt es bei Anwendungsbenutzern zu Verzögerungen bei der Antwortzeit. Um optimistische Parallelität zu unterstützen, übergeben getrennte ADO-Recordsets zwei Kopien der Daten vom Server an den Client. Die zweite Kopie wird vom Client verwendet, um das kleinste Updaterowset zu bestimmen, das beim Commit einer Änderung übergeben werden soll. Dies reduziert zwar den Datenverkehr von der Präsentationsebene zu den Daten, aber die zusätzliche Last der zweiten Kopie kann erheblich sein. Die Verwendung von Recordsets als einziges Mittel zum Übergeben aller Informationen führt daher dazu, dass doppelt so viele Daten zwischen Ebenen wie erforderlich übergeben werden, es sei denn, das Updaterowset wird von einer Präsentationsebene zurück an die Datenebene übergeben.
-   **Die Spalte Bereitstellung** stellt Probleme im Zusammenhang mit der Datenübergabe dar, wenn sowohl auf der Aufrufer- als auch auf der Komponentenseite des Netzwerks eine spezielle Technologie erforderlich ist. Die Verwendung von ADO-Recordsets erfordert beispielsweise, dass ADO-Komponenten sowohl auf dem Client als auch auf dem Server vorhanden sind. XML-Parser müssen auch auf beiden Seiten vorhanden sein, um zu vermeiden, dass Parser in Ihre Anwendungen codiert werden müssen.
-   **Die Spalte Komplexität** ist für alle vier Optionen angegeben und ist eine Frage der Präferenz oder vorherigen Programmiermodellerfahrung, die möglicherweise bereits in Ihrer Entwicklungsorganisation eingerichtet wurde. Einige Benutzer finden die Übergabe von Parametern umständlich und haben das Gefühl, dass dies dem Programmierproblem zu viel Komplexität hinzufügt. Wenn Sie nachverfolgen, welchen Parameter Sie behandeln, und sie alle in einem Bearbeitungsfenster sichtbar machen, kann dies zu einer erhöhten Komplexität führen, die von einigen Entwicklern als nicht verwaltet bezeichnet wird.

Die Parameterübergabemethode kann auch Vor- und Nachholungen aufweisen, z. B. die folgenden:

-   Parameter können die Verwaltung mehrerer Argumente und Argumenttypen sowie die Entscheidung umfassen, wann ein Recordset als Parameter geeignet ist.
-   ADO-Recordsets können hierarchische Beziehungen in Methodenparametern auf ein oder zwei Argumente reduzieren. Dies vereinfacht das Programmiermodell erheblich und unterstützt das Hinzufügen von Spalten zu einem späteren Zeitpunkt, aber es blendet auch die Informationshierarchie aus. Wenn Sie Informationen in ein ADO-Recordset einpacken und später extrahieren, müssen Sie die Namen der einzelnen Spalten kennen oder die Spalten reihenfolge kennen. Diese Situation kann die Komplexität für andere Komponenten- oder Anwendungsentwickler im Projekt erhöhen.
-   XML ist eine andere Drehung in der oben erwähnten verborgenen Hierarchiekomplikation. Der Programmierer muss die Verwendung eines XML-Parsers verstehen, um Zugriff auf die Informationen zu erhalten, und muss häufig die Namen der einzelnen Elemente im DataSet kennen, bevor das DataSet gefunden werden kann.
-   Arrays von -Strukturen führen zur Notwendigkeit eines gemeinsamen Verständnisses der Informationen, die sowohl vom Aufrufer als auch von der Komponente übergeben werden. Diese Notwendigkeit einer Zuordnung, die von zwei Systemelementen gemeinsam genutzt wird, kann zu Schwierigkeiten beim Umgang mit verschiedenen Versionen von Komponenten führen. Obwohl sich die Methodensignatur möglicherweise nicht ändert, können Änderungen an den erwarteten Informationen aufrufende Programme inkompatibel machen.

Da die Komplexitätsprobleme im Zusammenhang mit allen vier Methoden zur Parameterübergibtung so ähnlich sind, ist es unübersetzbar, dass es eine erhebliche Vereinfachungsmöglichkeit im Zusammenhang mit einer Auswahl gibt.

## <a name="using-a-factory-pattern-to-pass-data"></a>Verwenden eines Factorymusters zum Übergeben von Daten

Ein wichtiger Entwurfspunkt ist die Benutzerfreundlichkeit. In dem Moment, in dem Sie sich entschieden haben, ADO-Recordsets zu verwenden, um einen strukturierten Satz von Details an die Präsentationsebene zurückübertragen, haben Sie ein Komplexitätsproblem eingeführt. Programmierer der Präsentationsebene müssen die Struktur dieser Recordsets verstehen. Ein höheres Komplexitätsproblem kann auftreten, wenn Sie mehrere Details für eine Gruppe von Daten benötigen, die in einem Recordset übergeben werden sollen. Zur Vereinfachung sollten Sie erwägen, immer dann eine Recordset-Factorymethode zu erstellen, wenn Sie beabsichtigen, daten in strukturierten ADO-Recordsets zu übergeben.

Die Recordset-Factory sollte ein leeres, aber beschreibbares getrenntes Recordset an den Aufrufer zurückgeben. Dieses Recordset sollte die richtigen Felder (Namen und Datentypen) bereits konfiguriert haben, damit der aufrufende Client nicht wissen muss, wie das Recordset hergestellt werden soll. Dieser Ansatz wird häufig als *Factorymuster* bezeichnet und ist ein gängiges Lösungsmuster, das die Notwendigkeit löst, ein Objekt mit einer bestimmten Komplexität zu erstellen, ohne die Nuancen der Erstellung kennen zu müssen.

Einfache Entwurfsentscheidungen, z. B. das Auswählen des gleichen Parameternamens für denselben Datenteil für jede Methode, bei der diese Informationen übergeben werden, erleichtern es, eine Methode zu betrachten und zu wissen, was erwartet wird. Die Sicherstellung, dass die Reihenfolge, in der like-Argumente übergeben werden, über eine gesamte Methodenfamilie hinweg konsistent ist, stellt einen Komfortpunkt dar, der ein konsistentes Modell erzwingt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Optimieren von Interaktionen zwischen der COM+-Geschäftslogikebene und der Datenschicht](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




