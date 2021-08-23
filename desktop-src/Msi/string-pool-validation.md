---
description: Der Windows Installer speichert alle Datenbankzeichenfolgen in einem einzelnen freigegebenen Zeichenfolgenpool, um die Größe der Datenbank zu reduzieren und die Leistung zu verbessern.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: String-Pool-Überprüfung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e895a9e9032cb0cf5d94b5a8c3c9070c46fe79041dee41e4ea10366043b4af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627360"
---
# <a name="string-pool-validation"></a>String-Pool-Überprüfung

Der Windows Installer speichert alle Datenbankzeichenfolgen in einem einzelnen freigegebenen Zeichenfolgenpool, um die Größe der Datenbank zu reduzieren und die Leistung zu verbessern. Die einzige Möglichkeit zum Überprüfen des Zeichenfolgenpools ist die Verwendung des MsiInfo-Tools, das sich im Windows Installer SDK befindet.

Die Überprüfung des Zeichenfolgenpools besteht aus zwei Hauptüberprüfungen:

-   [DBCS-Zeichenfolgentests](#dbcs-string-tests)
-   [Überprüfung der Verweisanzahl](#reference-count-verification)

## <a name="dbcs-string-tests"></a>DBCS-Zeichenfolgentests

Die DBCS-Zeichenfolge überprüft jede Zeichenfolge in der Datenbank auf zwei Kriterien: Wenn ein Zeichen ein erweitertes Zeichen ist (größer als 127), wird bei Paketen mit einer neutralen Codepage die Zeichenfolge gekennzeichnet, und es wird eine Meldung angezeigt, die angibt, dass die Codepage der Datenbank ungültig ist, da diese Zeichen erfordern, dass eine bestimmte Codepage auf allen Systemen konsistent gerendert wird.

Wenn die Datenbank über eine Codepage verfügt, wird jede Zeichenfolge auf einen ungültigen DBCS-Indikator überprüft. Wenn eine nicht neutrale Zeichenfolge nicht ordnungsgemäß markiert wurde, werden die Zeichen nicht ordnungsgemäß gerendert. (Dies wird am häufigsten dadurch verursacht, dass die Codepage mithilfe von auf einen bestimmten Wert erzwungen wird. \_ ForceCodepage-Tabelle mit nicht neutralen Zeichenfolgen, die bereits in der Datenbank enthalten sind.) Beachten Sie, dass diese Überprüfung erfordert, dass die Codepage der Datenbank auf dem System installiert ist.

Bei einem Codepageproblem kann der Benutzer den Fehler mithilfe der Tabelle ForceCodepage beheben, um die Codepage der Datenbank auf den entsprechenden \_ Wert zu erzwingen. Weitere Informationen finden Sie unter [Codepagebehandlung.](code-page-handling-windows-installer-.md)

## <a name="reference-count-verification"></a>Überprüfung der Verweisanzahl

Um die Verweisanzahl aller Zeichenfolgen zu überprüfen, wird jede Tabelle auf Zeichenfolgenwerte überprüft, die Anzahl jeder einzelnen Zeichenfolge wird beibehalten, und das Ergebnis wird mit der gespeicherten Verweisanzahl im Datenbank-Zeichenfolgenpool verglichen.

Wenn ein Problem mit der Anzahl von Zeichenfolgenverweisen besteht, sollte der Benutzer sofort jede Tabelle der Datenbank mit [**msiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)exportieren, eine neue Datenbank erstellen und die Tabellen mit [**msiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)in die neue Datenbank importieren. Die neue Datenbank hat dann den gleichen Inhalt wie die alte Datenbank, aber die Anzahl der Zeichenfolgenverweise ist richtig. Das Hinzufügen oder Löschen von Daten aus einer Datenbank mit einem beschädigten Zeichenfolgenpool kann die Beschädigung der Datenbank und den Verlust von Daten erhöhen. Daher ist es wichtig, diese Schritte schnell zu ergreifen, um weiteren Datenverlust zu verhindern.

Denken Sie beim Neuerstellen von Datenbanken daran, alle erforderlichen Speicher und Streams in die neue Datenbank einbetten (siehe [ \_ Streams](-streams-table.md) Table and [ \_ Storages Table](-storages-table.md)), und beachten Sie Probleme mit der Codepage. Denken Sie auch daran, die erforderlichen Eigenschaften des [Zusammenfassungsinformationsstreams](summary-information-stream.md) zu festlegen.

 

 



