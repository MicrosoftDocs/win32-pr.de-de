---
description: In diesem Abschnitt werden die Windows Shell-Pfadbehandlungsfunktionen beschrieben. Die in dieser Dokumentation erläuterten Programmierelemente werden von Shlwapi.dll exportiert und in Shlwapi.h und Shlwapi.lib definiert.
title: Shellpfadbehandlungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 90937e4aa3c93c14957ec0db7f081c1cb598989e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481966"
---
# <a name="shell-path-handling-functions"></a>Shellpfadbehandlungsfunktionen

In diesem Abschnitt werden die Windows Shell-Pfadbehandlungsfunktionen beschrieben. Die in dieser Dokumentation erläuterten Programmierelemente werden von Shlwapi.dll exportiert und in Shlwapi.h und Shlwapi.lib definiert.

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a><br /> | Fügt einen zurücken Schrägstrich am Ende einer Zeichenfolge hinzu, um die richtige Syntax für einen Pfad zu erstellen. Wenn der Quellpfad bereits über einen nach trailing backslash verfügt, wird kein zurückgesetzter Schrägstrich hinzugefügt. <br /><blockquote>[!Note]<br />Ein Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash-</strong></a> oder <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx-Funktion</strong></a> zu verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a><br /> | Fügt einer Pfadzeichenfolge eine Dateierweiterung hinzu.<br /><blockquote>[!Note]<br />Ein Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension-Funktion</strong></a> zu verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a><br /> | Fügt einen Pfad an das Ende eines anderen an. <br /><blockquote>[!Note]<br />Ein Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend-</strong></a> oder <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx-Funktion</strong></a> zu verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a><br /> | Erstellt einen Stammpfad aus einer angegebenen Laufwerknummer.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a><br /> | Vereinfacht einen Pfad, indem Navigationselemente wie "." und "." entfernt werden, um einen direkten, wohlgeformten Pfad zu erzeugen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a><br /> | Verkettet zwei Zeichenfolgen, die ordnungsgemäß gebildete Pfade darstellen, zu einem Pfad. verkettet auch alle relativen Pfadelemente. <br /><blockquote>[!Note]<br />Ein Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine-</strong></a> oder <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx-Funktion</strong></a> zu verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a><br /> | Vergleicht zwei Pfade, um zu bestimmen, ob sie ein gemeinsames Präfix verwenden. Ein Präfix ist einer dieser Typen: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a><br /> | Schneidt einen Dateipfad so ab, dass er in eine bestimmte Pixelbreite passt, indem Pfadkomponenten durch Ellipsen ersetzt werden.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a><br /> | Schneidt einen Pfad so ab, dass er in eine bestimmte Anzahl von Zeichen passt, indem Pfadkomponenten durch Ellipsen ersetzt werden.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a><br /> | Konvertiert eine Datei-URL in einen Microsoft MS-DOS-Pfad.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a><br /> | Erstellt einen Pfad aus einer Datei-URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a><br /> | Bestimmt, ob ein Pfad zu einem Dateisystemobjekt, z. B. einer Datei oder einem Ordner, gültig ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a><br /> | Durchsucht einen Pfad nach einer Erweiterung.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a><br /> | Durchsucht einen Pfad nach einem Dateinamen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a><br /> | Analysiert einen Pfad und gibt den Teil dieses Pfads zurück, der dem ersten schrägen Schrägstrich folgt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a><br /> | Sucht nach einer Datei.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a><br /> | Bestimmt, ob ein angegebener Dateiname über eines einer Liste von Suffixen verfügt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a><br /> | Sucht die Befehlszeilenargumente innerhalb eines angegebenen Pfads.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a><br /> | Bestimmt den Typ des Zeichens in Bezug auf einen Pfad.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a><br /> | Durchsucht einen Pfad nach einem Laufwerkbuchstaben im Bereich von "A" bis "Z" und gibt die entsprechende Laufwerknummer zurück.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a><br /> | Bestimmt, ob der registrierte Inhaltstyp einer Datei dem angegebenen Inhaltstyp entspricht. Diese Funktion erhält den Inhaltstyp für den angegebenen Dateityp und vergleicht diese Zeichenfolge mit <em>pszContentType.</em> Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a><br /> | Überprüft, ob ein Pfad ein gültiges Verzeichnis ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a><br /> | Bestimmt, ob ein angegebener Pfad ein leeres Verzeichnis ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a><br /> | Durchsucht einen Pfad nach pfadtrennenden Zeichen (z. B. ":" oder " \' ). Wenn keine pfadtrennenden Zeichen vorhanden sind, wird der Pfad als Dateispezifikationspfad betrachtet.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a><br /> | Bestimmt, ob eine Datei eine HTML-Datei ist. Die Ermittlung erfolgt basierend auf dem Inhaltstyp, der für die Erweiterung der Datei registriert ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a><br /> | Bestimmt, ob ein Dateiname im langen Format vor liegt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a><br /> | Bestimmt, ob eine Pfadzeichenfolge eine Netzwerkressource darstellt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a><br /> | Durchsucht einen Pfad, um zu bestimmen, ob er ein gültiges Präfix des typs enthält, der von <em>pszPrefix übergeben wird.</em> Ein Präfix ist einer dieser Typen: "C: \\ ", ".", "..", ".. \\ ".<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a><br /> | Durchsucht einen Pfad und bestimmt, ob er relativ ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a><br /> | Bestimmt, ob eine Pfadzeichenfolge auf den Stamm eines Volumes verweist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a><br /> | Vergleicht zwei Pfade, um zu bestimmen, ob sie über eine gemeinsame Stammkomponente verfügen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a><br /> | Bestimmt, ob ein vorhandener Ordner die Attribute enthält, die ihn zu einem Systemordner machen. Alternativ gibt diese Funktion an, ob bestimmte Attribute einen Ordner als Systemordner qualifizieren.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a><br /> | Bestimmt, ob eine Pfadzeichenfolge ein gültiger UNIVERSAL NAMING CONVENTION (UNC)-Pfad ist, im Gegensatz zu einem Pfad, der auf einem Laufwerkbuchstaben basiert.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a><br /> | Bestimmt, ob eine Zeichenfolge nur für einen Serverpfad eine gültige UNC-Zeichenfolge ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a><br /> | Bestimmt, ob eine Zeichenfolge ein gültiger UNC-Freigabepfad ist, \\ <em>Serverfreigabe</em> \<em> </em> .<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a><br /> | Testet eine bestimmte Zeichenfolge, um zu ermitteln, ob sie einem gültigen URL-Format entspricht.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a><br /> | Konvertiert einen Pfad in Großbuchstaben in alle Kleinbuchstaben, um dem Pfad eine konsistente Darstellung zu verleihen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a><br /> | Gibt einem vorhandenen Ordner die richtigen Attribute, um ein Systemordner zu werden.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br /> | Durchsucht eine Zeichenfolge mithilfe eines MS-DOS-Platzhalter-Übereinstimmungstyps.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a><br /> | Entspricht einem Dateinamen aus einem Pfad mit mindestens einem Dateinamensmuster.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a><br /> | Analysiert eine Dateispeicherortzeichenfolge, die einen Dateispeicherort und einen Symbolindex enthält, und gibt separate Werte zurück.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a><br /> | Durchsucht einen Pfad nach Leerzeichen. Wenn Leerzeichen gefunden werden, wird der gesamte Pfad in Anführungszeichen eingeschlossen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a><br /> | Erstellt einen relativen Pfad von einer Datei oder einem Ordner zu einer anderen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a><br /> | Entfernt alle Argumente aus einem angegebenen Pfad.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a><br /> | Entfernt den nach folgenden schrägen Schrägstrich aus einem angegebenen Pfad.<br /><blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Es wird empfohlen, die <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>Funktion PathCchRemoveBackslash</strong></a> oder <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> zu verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a><br /> | Entfernt alle führenden und nachstellenden Leerzeichen aus einer Zeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a><br /> | Entfernt die Dateinamenerweiterung aus einem Pfad, sofern vorhanden. <br /><blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Wir empfehlen die Verwendung von <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension.</strong></a></blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a><br /> | Entfernt den Nachnamen der Datei und den schrägen Schrägstrich aus einem Pfad, sofern vorhanden.<br /><blockquote>[!Note]<br />Diese Funktion ist als veraltet markiert. Wir empfehlen die Verwendung der <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec-Funktion.</strong></a></blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a><br /> | Ersetzt die Erweiterung eines Dateinamens durch eine neue Erweiterung. Wenn der Dateiname keine Erweiterung enthält, wird die Erweiterung am Ende der Zeichenfolge angefügt.<br /><blockquote>[!Note]<br />Ein Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension-Funktion</strong></a> zu verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a><br /> | Bestimmt, ob ein angegebener Pfad ordnungsgemäß formatiert und vollqualifiziert ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a><br /> | Legt den Text eines untergeordneten Steuerelements in einem Fenster oder Dialogfeld fest, indem <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> verwendet wird, um sicherzustellen, dass der Pfad in das Steuerelement passt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a><br /> | Ruft einen Zeiger auf das erste Zeichen in einem Pfad ab, der auf den Laufwerkbuchstaben oder UNC-Server-/Freigabepfadelemente folgt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a><br /> | Entfernt den Pfadteil eines vollqualifizierten Pfads und einer vollqualifizierten Datei.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a><br /> | Entfernt alle Datei- und Verzeichniselemente in einem Pfad mit Ausnahme der Stamminformationen.<br /><blockquote>[!Note]<br />Ein Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot-Funktion</strong></a> zu verwenden.</blockquote><br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a><br /> | Entfernt die Dekoration aus einer Pfadzeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a><br /> | Ersetzt bestimmte Ordnernamen in einem vollqualifizierten Pfad durch die zugeordnete Umgebungszeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a><br /> | Entfernt die Attribute aus einem Ordner, der ihn zu einem Systemordner macht. Dieser Ordner muss tatsächlich im Dateisystem vorhanden sein.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a><br /> | Entfernt Anführungszeichen am Anfang und Ende eines Pfads.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a><br /> | Überprüft einen Bindungskontext, um zu prüfen, ob eine Bindung an ein bestimmtes Komponentenobjekt sicher ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a><br /> | Bestimmt ein Schema für eine angegebene URL-Zeichenfolge und gibt eine Zeichenfolge mit einem entsprechenden Präfix zurück.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br /> | Konvertiert eine URL-Zeichenfolge in ein kanonisches Format.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a><br /> | Wenn sie mit einem -relative URL und seiner Basis bereitgestellt wird, gibt eine URL in kanonischer Form zurück.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a><br /> | Vergleicht zwei URL-Zeichenfolgen mit Schreibung.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a><br /> | Konvertiert einen MS-DOS-Pfad in eine kanonische URL.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a><br /> | Konvertiert Zeichen oder Ersatzzeichenpaare in einer URL, die während des Transports über das Internet geändert werden können ("unsichere" Zeichen) in die entsprechenden Escapesequenzen. Ersatzzeichenpaare sind Zeichen zwischen U+10000 bis U+10FFFF (in UTF-32) oder zwischen DC00 und DFFF (in UTF-16). <br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a><br /> | Ein Makro, das Leerzeichen in die entsprechende Escapesequenz konvertiert.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a><br /> | Ruft den Speicherort aus einer URL ab.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a><br /> | Akzeptiert eine URL-Zeichenfolge und gibt einen angegebenen Teil dieser URL zurück.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a><br /> | Hasht eine URL-Zeichenfolge.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>URLIs</strong></a><br /> | Testet, ob eine URL ein angegebener Typ ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a><br /> | Testet eine URL, um festzustellen, ob es sich um eine Datei-URL handelt.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a><br /> | Gibt zurück, ob eine URL eine URL ist, die Browser in der Regel nicht im Navigationsverlauf enthalten.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a><br /> | Gibt zurück, ob eine URL nicht transparent ist.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a><br /> | Konvertiert Escapesequenzen zurück in normale Zeichen.<br /> | 
| <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a><br /> | Konvertiert Escapesequenzen zurück in normale Zeichen und überschreibt die ursprüngliche Zeichenfolge.<br /> | 




 

 

 




