---
description: Der Windows Installer speichert alle Daten Bank Zeichenfolgen in einem einzelnen freigegebenen Zeichen folgen Pool, um die Größe der Datenbank zu reduzieren und die Leistung zu verbessern.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: String-Pool Validierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130277"
---
# <a name="string-pool-validation"></a>String-Pool Validierung

Der Windows Installer speichert alle Daten Bank Zeichenfolgen in einem einzelnen freigegebenen Zeichen folgen Pool, um die Größe der Datenbank zu reduzieren und die Leistung zu verbessern. Die einzige Möglichkeit, den Zeichen folgen Pool zu validieren, ist die Verwendung des Msiinfo-Tools, das im Windows Installer SDK gefunden wurde.

Die Überprüfung des Zeichen folgen Pools besteht aus zwei Hauptprüfungen:

-   [DBCS-Zeichen folgen Tests](#dbcs-string-tests)
-   [Verweis Zähler Überprüfung](#reference-count-verification)

## <a name="dbcs-string-tests"></a>DBCS-Zeichen folgen Tests

Die DBCS-Zeichen folgen Tests Scannen jede Zeichenfolge in der Datenbank auf zwei Kriterien: Wenn ein beliebiges Zeichen ein erweitertes Zeichen (größer als 127) ist, wird die Zeichenfolge gekennzeichnet, und es wird eine Meldung angezeigt, die besagt, dass die Codepage der Datenbank ungültig ist, da diese Zeichen erfordern, dass eine bestimmte Codepage auf allen Systemen konsistent gerendert wird.

Wenn die Datenbank über eine Codepage verfügt, wird jede Zeichenfolge auf einen ungültigen DBCS-Indikator überprüft. Wenn eine nicht neutrale Zeichenfolge nicht ordnungsgemäß markiert wurde, werden die Zeichen nicht korrekt dargestellt. (Dies wird in der Regel durch erzwingen der Codepage zu einem bestimmten Wert verursacht, indem Sie das \_ Forcecodepage-Tabelle mit nicht neutralen Zeichen folgen, die sich bereits in der Datenbank befinden.) Beachten Sie, dass diese Überprüfung erfordert, dass die Codepage der Datenbank auf dem System installiert ist.

Wenn ein Code Page Problem vorliegt, kann der Benutzer den Fehler möglicherweise beheben, indem er die \_ forcecodepage-Tabelle verwendet, um die Codepage der Datenbank auf den entsprechenden Wert zu erzwingen. Weitere Informationen finden Sie unter [Code Page Handling](code-page-handling-windows-installer-.md).

## <a name="reference-count-verification"></a>Verweis Zähler Überprüfung

Zum Überprüfen der Verweis Anzahl aller Zeichen folgen wird jede Tabelle auf Zeichen folgen Werte überprüft, die Anzahl der einzelnen Zeichen folgen wird beibehalten, und das Ergebnis wird mit dem gespeicherten Verweis Zähler im Daten Bank Zeichenfolgen-Pool verglichen.

Wenn ein Problem mit der Zeichenfolge Verweis Zählung vorliegt, sollte der Benutzer jede Tabelle der Datenbank sofort mithilfe von " [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)" exportieren, eine neue Datenbank erstellen und die Tabellen mithilfe von " [**msidatabaseimport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)" in die neue Datenbank importieren. Die neue Datenbank hat dann denselben Inhalt wie die alte Datenbank, aber die Anzahl der Zeichen folgen Verweise ist richtig. Durch das Hinzufügen oder Löschen von Daten aus einer Datenbank mit einem beschädigten Zeichen folgen Pool kann die Beschädigung der Datenbank und des Daten Verlusts erhöht werden. Daher ist es wichtig, diese Schritte schnell auszuführen, um weiteren Datenverlust zu verhindern.

Beachten Sie beim Neuerstellen von Datenbanken, dass alle erforderlichen Speicher-und Datenströme in die neue Datenbank eingebettet werden (siehe Tabelle " [ \_ Streams Table](-streams-table.md) " und " [ \_ Speicher Table](-storages-table.md)"), und beachten Sie die Probleme mit der Denken Sie auch daran, die erforderlichen Eigenschaften für [Zusammenfassungs Informationsdaten Ströme](summary-information-stream.md) festzulegen.

 

 



