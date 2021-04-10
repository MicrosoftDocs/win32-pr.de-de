---
description: Anwendungen schreiben Endbenutzer definierte Zeichen (eudcs) und private Verwendungs Bereiche (Pua) auf den Bildschirm oder Drucker, ebenso wie Sie andere Zeichen schreiben, indem Sie Ausgabefunktionen wie z. b. TextOut und exttextout verwenden.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Schreiben, Mapping und Sortieren von EUDC-und Pua-Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c34264d956bb6a87407e249f68b2bc03fb2c99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214634"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Schreiben, Mapping und Sortieren von EUDC-und Pua-Zeichen

Anwendungen schreiben Endbenutzer definierte Zeichen (eudcs) und private Verwendungs Bereiche (Pua) auf den Bildschirm oder Drucker, ebenso wie Sie andere Zeichen schreiben, indem Sie Ausgabefunktionen wie z. b. [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) und [exttextout](/windows/win32/api/wingdi/nf-wingdi-exttextouta)verwenden. Diese Funktionen rufen automatisch Zeichen Informationen von EUDC oder Pua-Zeichen Schriftarten ab, wenn EUDC aktiviert ist. Weitere Informationen finden Sie unter [Endbenutzer \_ definierte und private Verwendungs Bereichs Zeichen](end-user-defined-characters.md).

Beim Schreiben von eudcs oder Pua-Zeichen hängt der Vorgang der Textausgabe Funktion von der aktuell ausgewählten Schriftart ab. Wenn es sich bei der ausgewählten Schriftart um eine integrierte EUDC-oder Pua-Zeichen Schriftart handelt, ruft die Funktion Zeichen Informationen aus dieser Schriftart ab. Wenn es sich bei der ausgewählten Schriftart um eine DBCS-TrueType-Schriftart ( [Double-Byte Character Set](double-byte-character-sets.md) ) handelt, der eine separate EUDC-Schriftart zugeordnet ist, ruft die Funktion Informationen aus der angegebenen EUDC-Schriftart ab. Wenn es sich bei der ausgewählten Schriftart um eine [Unicode](unicode.md) -TrueType-Schriftart handelt, die eine separate Pua-Zeichen Schriftart aufweist, ruft die Funktion Informationen aus der Pua-Zeichen Schriftart ab. Wenn der ausgewählten Schriftart keine EUDC-oder Pua-Zeichen Schriftart zugeordnet ist, ruft die Funktion Informationen aus der Standard Schriftart des standardmäßigen EUDC des Systems ab. Wenn sich das Zeichen nicht in der Standard Schriftart des standardmäßigen EUDC-Systems befindet oder keine standardmäßige EUDC-Standard Schriftart vorhanden ist, schreibt die Funktion das Standard Zeichen, das von der ausgewählten Schriftart definiert wird.

Anwendungen können eudcs mithilfe der Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) zu und aus Unicode zuordnen. Die **multibyteabwidechar** -Funktion ordnet die meisten eudcs Zeichen in der Unicode-Pua zu. Zur Unterstützung bestimmter nationaler oder regionaler Standards können jedoch einige eudcs nicht-Pua-Unicode-Code Punkten zugeordnet werden. Die **WideCharToMultiByte** -Funktion ordnet der EUDC-Entsprechung ein Zeichen in der Pua zu, wenn eine solche Zuordnung vorhanden ist und der Codepunkt nicht über eine gültige nicht-Pua-Zuordnung in Unicode verfügt. Nicht alle Codepages haben einen EUDC-Bereich. Die in einem-Befehl von **WideCharToMultiByte** angegebene Codepage muss einen EUDC-Code Bereich enthalten, damit die Zuordnung zum EUDC-Bereich erfolgen darf. Wenn die Codepage keinen EUDC-Code Bereich enthält, ruft die Funktion das Standard Zeichen für beliebige Zeichen in der Unicode-Pua ab.

" [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) " und " [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) " garantieren keine Roundtrip-Zuordnung. Anders ausgedrückt: Es ist möglich, mit einer bestimmten Multibytezeichen-Zeichenfolge zu beginnen, die eudcs enthält, ordnen Sie die Zeichenfolge mit **MultiByteToWideChar** Unicode zu, und ordnen Sie Sie dem ursprünglichen DBCS mit **WideCharToMultiByte** zu. Schließlich wird ein Ergebnis angezeigt, das nicht mit der ursprünglichen Zeichenfolge identisch ist. Anwendungen, die sich auf die Zuordnung von eudcs zu Unicode verlassen, sollten sicherstellen, dass alle erforderlichen Zeichen zwischen dem entsprechenden Codepage-EUDC-Bereich und dem Unicode-Pua aufgerundet werden.

Anwendungen sollten nicht versuchen, eudcs von einer Codepage zu einer anderen zuzuordnen. Wenn eine Anwendung mit einem EUDC von einer Codepage gestartet wird, Sie in Unicode mit [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)zuordnet und einem anderen DBCS mit [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)zugeordnet ist, gibt es keine Garantie für die Ergebnisse. Das ursprüngliche Zeichen kann einem anderen EUDC auf der Ziel Codepage zugeordnet werden, oder es kann als nicht definiertes Zeichen zugeordnet werden. Ebenso kann das Mapping einer Unicode-Zeichenfolge zu einer Codepage mit einem EUDC-Bereich unbeabsichtigte Ergebnisse aufweisen. Wenn die Unicode-Zeichenfolge einen Pua-Codepunkt enthält, ist es möglich, dass der Codepunkt einem EUDC zugeordnet wird, der nicht das gleiche Zeichen darstellt.

Anwendungen können DBCS-Zeichen folgen, die eudcs enthalten, mithilfe der ANSI-Version der [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) -Funktion vergleichen. Die-Funktion ordnet die Zeichen vor dem Vergleich von Zeichen Werten den Unicode-Zeichen zu. Anwendungen können einen Sortierschlüssel für die Zeichenfolge erstellen, indem Sie die ANSI-Version der [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) -Funktion und den lcmap \_ SortKey-Wert verwenden. Mit dieser Funktion werden Zeichen zuerst Unicode-Zeichen zugeordnet. Alle Zeichen im Pua werden nach allen anderen Unicode-Zeichen sortiert. Innerhalb des Bereichs werden Zeichen in numerischer Reihenfolge sortiert. Wenn eine Anwendung versucht, CType-Informationen für einen EUDC mithilfe der [getstringtypea](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) -Funktion abzurufen, ruft die Funktion für jedes Zeichen **null** ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
