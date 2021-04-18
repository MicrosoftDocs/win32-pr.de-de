---
description: In der Regel unterscheidet sich die Latenz zwischen den Ebenen einer verteilten Anwendung erheblich.
ms.assetid: 4780a9fd-5940-4b10-a596-22214b17c033
title: Optimieren von Interaktionen zwischen der com+-Geschäftslogik Ebene und der Präsentationsebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe6094cb12cc7875d8a18dea3d28ac55bf8d6ae2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345628"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-presentation-tier"></a>Optimieren von Interaktionen zwischen der com+-Geschäftslogik Ebene und der Präsentationsebene

In der Regel unterscheidet sich die Latenz zwischen den Ebenen einer verteilten Anwendung erheblich. Aufrufe zwischen der Präsentations-und der Geschäftslogik Ebene sind häufig eine Größenordnung langsamer als Aufrufe zwischen der Geschäfts-und der Datenebene. Dies hat zur Folge, dass der Status "aufrechterhalten" beim Aufrufen der Geschäftslogik Schicht teurer ist.

In den folgenden Themen werden Methoden zum Übergeben von Daten zwischen der Präsentations-und der Geschäftslogik Ebene erläutert:

-   [Übergeben von Parametern](#passing-parameters)
-   [Optionen für die Daten Übergabe](#data-passing-options)
-   [Verwenden eines Factorymusters zum Übergeben von Daten](#using-a-factory-pattern-to-pass-data)
-   [Zugehörige Themen](#related-topics)

## <a name="passing-parameters"></a>Übergeben von Parametern

Damit eine bestimmte Gruppe von Informationen zwischen der Präsentations-und der Geschäftslogik Schicht übergeben werden kann, haben Sie möglicherweise eine einzelne Zeile, mehrere Zeilen oder eine Kombination aus einer einzelnen Zeile (z. b. eine Kopfzeile) und mehrere Detail Zeilen von Daten. Die effizienteste Methode, um diese Informationen zwischen den Ebenen zu übergeben, ist ein einzelner Methoden Aufruf. Mit diesem einzelnen-Befehl wird der gesamte zu über gebenden Informations Satz verwaltet. Dies ist erforderlich, es sei denn, Sie entscheiden sich für die Steuerung der Transaktion auf der Präsentationsebene (und machen die gesamte Transaktions Behandlung in der Präsentationsebene in der Funktion identisch). Microsoft empfiehlt nicht, Transaktionen aus der Präsentationsebene durchzuführen, da Aufrufe zwischen dieser Ebene und der Geschäftslogik Ebene in der Regel die langsamste von Aufrufen in einer Anwendung mit mehreren Ebenen sind.

Eine Möglichkeit zum Erstellen einer solchen Methode besteht darin, einzelne Zeilen von Informationen als Parameter zu übergeben und mehrere Zeilen als ADO-Recordsets zu übergeben. Recordsets sind der Kern der ADO-Datenzugriffs Methodik von Microsoft, und die Verwendung von ADO-Recordsets ermöglicht es Ihnen, alle Informationen, die mit einer einzelnen Transaktion verknüpft sind, in einem Schritt zu übergeben.

## <a name="data-passing-options"></a>Optionen für die Daten Übergabe

Beim Übergeben von Daten sind andere Optionen zu beachten. Hierzu gehören die Verwendung einer Liste von Parametern und ADO-Recordsets (wie oben erläutert), nur ADO-Recordsets, XML-codierte Zeichen folgen oder Arrays von Strukturen. In diesem Abschnitt werden die einzelnen Optionen erläutert.

In der folgenden Tabelle sind Bereiche aufgeführt, in denen bei der Verwendung einer der vier verschiedenen Argument Übergabe Möglichkeiten besonders sorgfältig vorgegangen werden muss. Ein "X" steht für Bereiche, in denen Kompromisse verstanden und gegen die Anforderungen der einzelnen Projekte abgewogen werden müssen. Versuchen Sie nicht, auf Komponentenbasis Entscheidungen zu treffen. Die Vorteile eines konsistenten Programmiermodells in einem Projekt überwiegen weitgehend den Vorteil der Optimierung von pro-Methode oder pro Komponente in allen bis auf die extremsten Umstände. Die Spalten werden in der Liste beschrieben, die auf die Tabelle folgt.



|                       | Parallelität  | WAN          | Bereitstellung   | Komplexität   |
|-----------------------|--------------|--------------|--------------|--------------|
| Eingabe | Wert |
| Recordsets<br/> |              | X<br/> | X<br/> | X<br/> |
| XML<br/>        | X<br/> |              | X<br/> | X<br/> |
| Arrays<br/>     | X<br/> |              | X<br/> | X<br/> |



 

Die vier Spalten definieren Bereiche, die bei Verwendung dieser Option zum Übergeben von Parametern überwacht werden sollen.

-   **Die** Parallelitäts Spalte stellt den Bedarf für das Codieren oder Bereitstellen eines Mechanismus dar, mit dem Sperr Bedingungen bei Update Vorgängen verwaltet werden. Da Methoden, die speichern ausführen, Updates darstellen können, können Parallelitäts Probleme auftreten. Zwei Arten von Sperren sind in der vollständigen und pessimistischen Situation. Durch pessimistische sperren wird verhindert, dass ein Benutzerdaten für die Aktualisierung erhält, während ein anderer Benutzer die Möglichkeit hat, ein Update auszuführen. Die optimistische Sperre unterstützt viele weitere Benutzer, indem Sie gegen die Wahrscheinlichkeit, dass zwei Benutzer das gleiche Dokument gleichzeitig aktualisieren würden, den Handel unterstützt. Optimistische Sperr Aufrufe, um zu überprüfen, ob die gespeicherten Daten mit den Daten zu dem Zeitpunkt übereinstimmen, zu dem auf eine Kopie der Daten zugegriffen wurde, um Sie zu ändern. ADO-Recordsets bieten automatische Unterstützung für die optimistische Sperrung. Aktualisierungs Szenarios mit einzelnen Zeilen Parameterlisten bieten keine ausreichende Unterstützung für die Parallelitäts Überprüfung. XML hat dieses Problem, da kein Sperr Bewusstsein in XML-Daten vorhanden ist.
-   **Die WAN-Spalte** stellt Bedingungen dar, bei denen in einem WAN (Wide Area Network) Übertragungs Konflikte auftreten können. Wenn das WAN nicht über genügend Kapazität verfügt, um alle Daten zu verwalten, die zu einem beliebigen Zeitpunkt verschoben werden, treten bei Anwendungs Benutzern Reaktionszeit Verzögerungen auf. Um optimistische Parallelität zu unterstützen, übergeben getrennte ADO-Recordsets zwei Kopien der Daten vom Server an den Client. Die zweite Kopie wird vom Client verwendet, um das kleinste updaterrowset zu bestimmen, das zurückgegeben werden soll, wenn ein Commit für eine Änderung ausgeführt wird. Während dies den Datenverkehr von der Präsentationsebene zu den Daten reduziert, kann die zusätzliche Auslastung der zweiten Kopie beträchtlich sein. Die Verwendung von Recordsets als alleinige Methode, alle Informationen zu übergeben, bewirkt daher, dass doppelt so viele Daten wie erforderlich zwischen den Ebenen übergeben werden, es sei denn, das Aktualisierungs-Rowset wird von einer Präsentationsebene an die Datenebene zurückgegeben.
-   **Die Bereitstellungs Spalte** stellt Probleme dar, die mit der Daten Übergabe verbunden sind, wenn auf dem Aufrufer und der Komponenten Seite des Netzwerks eine spezielle Technologie erforderlich ist. Beispielsweise erfordert die Verwendung von ADO-Recordsets, dass ADO-Komponenten sowohl auf dem Client als auch auf dem Server vorhanden sind. XML-Parser müssen auch auf beiden Seiten vorhanden sein, um zu vermeiden, dass Sie Parser in Ihre Anwendungen codieren müssen.
-   **Die Spalte Komplexität** wird für alle vier Optionen angezeigt, und Sie ist ein bevorzugtes oder Vorheriges Programmiermodell, das möglicherweise bereits in Ihrer Entwicklungsorganisation festgelegt ist. Einige Leute finden die Parameter Übergabe als umständlich und fühlen sich zu viel Komplexität des Programmier Problems. Die Nachverfolgung des Parameters, den Sie behandeln und der alle in einem Bearbeitungsfenster sichtbar ist, kann eine logistische Komplexität schaffen, die einige Entwickler nicht verwaltbar finden.

Die Parameter-Passing-Methode kann auch Kompromisse aufweisen, wie z. b. die folgenden:

-   Parameter können die Verwaltung mehrerer Argumente und Argument Typen einschließen. Außerdem müssen Sie entscheiden, wann ein Recordset zu einem Parameter wird.
-   ADO-Recordsets können hierarchische Beziehungen in Methoden Parametern bis auf ein oder zwei Argumente Ausschneiden. Dadurch wird das Programmiermodell erheblich vereinfacht und das Hinzufügen von Spalten zu einem späteren Zeitpunkt unterstützt. die Informationshierarchie wird jedoch ebenfalls ausgeblendet. Das Durcharbeiten von Informationen in ein ADO-Recordset und spätere Extraktion besteht darin, die Namen der einzelnen Spalten zu kennen oder die Spaltenreihenfolge zu kennen. Diese Situation kann die Komplexität für andere Komponenten-oder Anwendungsentwickler im Projekt erhöhen.
-   XML ist ein anderes Dreh Ende der oben erwähnten ausgeblendeten Hierarchie Komplikation. Der Programmierer muss mit der Verwendung eines XML-Parsers vertraut sein, um Zugriff auf die Informationen zu erhalten, und häufig müssen die Namen der einzelnen Elemente im DataSet bekannt sein, damit das Dataset gefunden werden kann.
-   Arrays von Strukturen führen zu einem allgemeinen Verständnis der Informationen, die für den Teil des Aufrufers und der Komponente übergeben werden. Diese Anforderung für eine Zuordnung, die von zwei Systemelementen gemeinsam genutzt wird, kann zu Schwierigkeiten beim Umgang mit verschiedenen Versionen von Komponenten führen. Obwohl die Methoden Signatur nicht geändert werden kann, können durch Änderungen an den erwarteten Informationen Aufruf Programme nicht kompatibel sein.

Da die Komplexitäts Probleme, die mit allen vier Parametern übergeben werden, so ähnlich sind, ist es fraglich, dass es eine beträchtliche Vereinfachungs Chance mit einer Auswahl gibt.

## <a name="using-a-factory-pattern-to-pass-data"></a>Verwenden eines Factorymusters zum Übergeben von Daten

Ein wichtiger Entwurfspunkt ist die einfache Verwendung. In dem Moment, in dem Sie ADO-Recordsets verwenden, um einen strukturierten Satz von Details an die Präsentationsebene zurückzuleiten, haben Sie ein Komplexitäts Problem eingeführt. Programmierer der Präsentationsebene müssen die Struktur dieser Recordsets verstehen. Ein größeres Problem kann auftreten, wenn Sie mehrere Details für einen Datensatz benötigen, der in einem Recordset übermittelt werden soll. Um die Dinge zu vereinfachen, sollten Sie eine Recordset Factory-Methode erstellen, wenn Sie beabsichtigen, Daten in strukturierten ADO-Recordsets zu übernehmen.

Die recordsetfactory sollte ein leeres, aber beschreibbares, nicht mit dem Aufrufer getrennte Recordset zurückgeben. Für dieses Recordset sollten die richtigen Felder (Namen und Datentypen) bereits konfiguriert sein, damit der aufrufenden Client nicht wissen muss, wie das Recordset hergestellt werden muss. Diese Vorgehensweise wird häufig als *Factorymuster* bezeichnet und ist ein gängiges Lösungsmuster, das das Erstellen eines Objekts einer bestimmten Komplexität vereinfacht, ohne die Feinheiten der Erstellung kennen zu müssen.

Einfache Entwurfs Optionen, wie z. b. die Auswahl desselben Parameter namens für die gleichen Daten in jeder Methode, in der diese Informationen übergeben werden, erleichtern es, eine Methode zu betrachten und zu wissen, was erwartet wird. Sicherzustellen, dass die Reihenfolge, in der like-Argumente übergangen werden, über eine gesamte Methoden Familie hinweg konsistent ist, stellt einen Komfort Punkt dar, der ein konsistentes Modell erzwingt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Optimieren von Interaktionen zwischen der com+-Geschäftslogik Ebene und der Datenebene](optimizing-interactions-between-the-com--business-logic-tier-and-the-data-tier.md)
</dt> </dl>

 

 




