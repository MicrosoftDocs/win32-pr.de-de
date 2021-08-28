---
description: Anwendungen schreiben EUDCs (End-User-Defined Characters) und PUA-Zeichen (Private Use Area) genauso auf den Bildschirm oder Drucker, wie sie andere Zeichen schreiben, indem sie Ausgabefunktionen wie TextOut und ExtTextOut verwenden.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Schreiben, Zuordnen und Sortieren von EUDC- und PUA-Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ab43eb54055b97fe1823ad99467a4cd0b12a0a5fb971d52d225631cfd37ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102080"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Schreiben, Zuordnen und Sortieren von EUDC- und PUA-Zeichen

Anwendungen schreiben EUDCs (End-User-Defined Characters) und PUA-Zeichen (Private Use Area) genauso auf den Bildschirm oder Drucker, wie sie andere Zeichen schreiben, indem sie Ausgabefunktionen wie [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) und [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta)verwenden. Diese Funktionen rufen automatisch Zeicheninformationen aus EUDC- oder PUA-Zeichenschriftarten ab, wenn EUDC aktiviert ist. Weitere Informationen finden Sie unter [ \_ Endbenutzerdefinierte und private Verwendungsbereichszeichen.](end-user-defined-characters.md)

Beim Schreiben von EUDCs oder PUA-Zeichen hängt der Vorgang der Textausgabefunktion von der aktuell ausgewählten Schriftart ab. Wenn es sich bei der ausgewählten Schriftart um eine integrierte EUDC- oder PUA-Schriftart handelt, ruft die Funktion Zeicheninformationen aus dieser Schriftart ab. Wenn es sich bei der ausgewählten Schriftart um eine [TRUEType-Schriftart (Double-Byte Character Set,](double-byte-character-sets.md) DBCS) handelt, der eine separate EUDC-Schriftart zugeordnet ist, ruft die Funktion Informationen aus der angegebenen EUDC-Schriftart ab. Wenn es sich bei der ausgewählten Schriftart um eine [Unicode TrueType-Schriftart](unicode.md) handelt, der eine separate PUA-Zeichenschriftart zugeordnet ist, ruft die Funktion Informationen aus der PUA-Zeichenschriftart ab. Wenn der ausgewählten Schriftart kein EUDC- oder PUA-Zeichenschriftart zugeordnet ist, ruft die Funktion Informationen aus der standardmäßigen EUDC-Schriftart des Systems ab. Wenn das Zeichen nicht in der EUDC-Standardschriftart des Systems enthalten ist oder es keine EUDC-Standardschriftart des Systems gibt, schreibt die Funktion das durch die ausgewählte Schriftart definierte Standardzeichen.

Anwendungen können EUDCs mithilfe der Funktionen [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) Unicode zuordnen. Die **MultiByteToWideChar-Funktion** ordnet die meisten EUDCs Zeichen im Unicode-PUA zu. Um jedoch bestimmte nationale oder regionale Standards zu unterstützen, können einige EUDCs Nicht-PUA Unicode-Codepunkten zugeordnet werden. Die **WideCharToMultiByte-Funktion** ordnet ein Zeichen im PUA seiner EUDC-Entsprechung zu, wenn eine solche Zuordnung vorhanden ist und der Codepunkt keine gültige Nicht-PUA-Zuordnung in Unicode hat. Nicht alle Codepages verfügen über einen EUDC-Bereich. Die in einem Aufruf von **WideCharToMultiByte** angegebene Codepage muss einen EUDC-Codebereich enthalten, damit die Zuordnung zum EUDC-Bereich erfolgen kann. Wenn die Codepage keinen EUDC-Codebereich enthält, ruft die Funktion das Standardzeichen für alle Zeichen im Unicode-PUA ab.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) und [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) garantieren keine Roundtripzuordnung. Mit anderen Worten: Es ist möglich, mit einer bestimmten Multibytezeichenfolge zu beginnen, die EUDCs enthält, die Zeichenfolge unicode mit **MultiByteToWideChar** zuzuordnen und sie mit **WideCharToMultiByte** wieder dem ursprünglichen DBCS zuzuordnen und am Ende ein Ergebnis zu erzielen, das nicht mit der ursprünglichen Zeichenfolge identisch ist. Anwendungen, die EUDCs Unicode zuordnen, sollten sicherstellen, dass alle erforderlichen Zeichen einen Roundtrip zwischen dem entsprechenden Codepage-EUDC-Bereich und dem Unicode-PUA ermöglichen.

Anwendungen sollten nicht versuchen, EUDCs von einer Codepage einer anderen zuzuordnen. Wenn eine Anwendung mit einem EUDC von einer Codepage aus beginnt, sie unicode mit [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)zuweist und einem anderen DBCS mit [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)zugeordnet wird, gibt es keine Garantien für die Ergebnisse. Das ursprüngliche Zeichen kann einem anderen EUDC auf der Zielcodepage zugeordnet oder als nicht definiertes Zeichen zugeordnet werden. Ebenso kann das Zuordnen einer Unicode-Zeichenfolge zu einer Codepage, die über einen EUDC-Bereich verfügt, unbeabsichtigte Ergebnisse haben. Wenn die Unicode-Zeichenfolge einen PUA-Codepunkt enthält, ist es möglich, dass der Codepunkt einem EUDC zugeordnet wird, das nicht das gleiche Zeichen darstellt.

Anwendungen können DBCS-Zeichenfolgen, die EUDCs enthalten, mithilfe der ANSI-Version der [CompareString-Funktion](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) vergleichen. Die Funktion ordnet die Zeichen effektiv Unicode zu, bevor Zeichenwerte verglichen werden. Anwendungen können einen Sortierschlüssel für die Zeichenfolge erstellen, indem sie die ANSI-Version der [**LCMapString-Funktion**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) und den LCMAP \_ SORTKEY-Wert verwenden. Diese Funktion ordnet Zeichen zuerst Unicode zu. Alle Zeichen im PUA werden nach allen anderen Unicode-Zeichen sortiert. Innerhalb des Bereichs werden Zeichen in numerischer Reihenfolge sortiert. Wenn eine Anwendung versucht, CTYPE-Informationen für ein EUDC mithilfe der [GetStringTypeA-Funktion](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) abzurufen, ruft die Funktion **NULL** für jedes Zeichen ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Unicode und Zeichensätzen](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
