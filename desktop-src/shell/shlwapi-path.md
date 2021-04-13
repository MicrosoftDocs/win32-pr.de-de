---
description: In diesem Abschnitt werden die Windows Shell-Pfad Behandlungs Funktionen beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.
title: Shellpfad-Verarbeitungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995071"
---
# <a name="shell-path-handling-functions"></a>Shellpfad-Verarbeitungsfunktionen

In diesem Abschnitt werden die Windows Shell-Pfad Behandlungs Funktionen beschrieben. Die in dieser Dokumentation erläuterten Programmier Elemente werden von Shlwapi.dll exportiert und in "shlwapi. h" und "shlwapi. lib" definiert.

## <a name="in-this-section"></a>In diesem Abschnitt



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>Pathaddbackschräg Strich</strong></a><br/></td>
<td>Fügt einen umgekehrten Schrägstrich am Ende einer Zeichenfolge hinzu, um die korrekte Syntax für einen Pfad zu erstellen. Wenn der Quellpfad bereits einen nachfolgenden umgekehrten Schrägstrich enthält, wird kein umgekehrter Schrägstrich hinzugefügt. <br/>
<blockquote>
[!Note]<br />
Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>pathcchaddbackschräg Strich</strong></a> " oder " <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>pathcchaddbackslashex</strong></a> " zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>Pathaddextension</strong></a><br/></td>
<td>Fügt einer Pfad Zeichenfolge eine Dateinamenerweiterung hinzu.<br/>
<blockquote>
[!Note]<br />
Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>pathcchaddextension</strong></a> " zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a><br/></td>
<td>Fügt einen Pfad am Ende eines anderen ein. <br/>
<blockquote>
[!Note]<br />
Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Wir empfehlen die Verwendung der Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>pathcchappend</strong></a> " oder " <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>pathcchappdex</strong></a> ".
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>Pathbuildroot</strong></a><br/></td>
<td>Erstellt einen Stammpfad aus einer angegebenen Laufwerksnummer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>Pathcanonicalize</strong></a><br/></td>
<td>Vereinfacht einen Pfad, indem Navigationselemente wie &quot; . &quot; und. entfernt werden &quot; &quot; , um einen direkten, wohlgeformten Pfad zu erhalten.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>Pathcombine</strong></a><br/></td>
<td>Verkettet zwei Zeichen folgen, die ordnungsgemäß geformte Pfade zu einem Pfad darstellen. verkettet außerdem alle relativen Pfad Elemente. <br/>
<blockquote>
[!Note]<br />
Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>pathcchcombine</strong></a> " oder " <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>pathcchcombineex</strong></a> " zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>Pathcommonprefix</strong></a><br/></td>
<td>Vergleicht zwei Pfade, um zu bestimmen, ob Sie ein gemeinsames Präfix haben. Ein Präfix ist einer der folgenden Typen: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>Pathcompactpath</strong></a><br/></td>
<td>Verkürzt einen Dateipfad, der in eine bestimmte Pixel Breite passt, indem Pfad Komponenten durch Ellipsen ersetzt werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>Pathcompactpathex</strong></a><br/></td>
<td>Verkürzt einen Pfad, der in eine bestimmte Anzahl von Zeichen passt, indem Pfad Komponenten durch Ellipsen ersetzt werden.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>Pathkreatefromurl</strong></a><br/></td>
<td>Konvertiert eine Datei-URL in einen Microsoft MS-DOS-Pfad.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>Pathkreatefromurlzuweisung</strong></a><br/></td>
<td>Erstellt einen Pfad aus einer Datei-URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>Pathfilevorhanden</strong></a><br/></td>
<td>Bestimmt, ob ein Pfad zu einem Dateisystem Objekt (z. b. eine Datei oder ein Ordner) gültig ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>Pathfindextension</strong></a><br/></td>
<td>Durchsucht einen Pfad nach einer Erweiterung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>Pathfindfilename</strong></a><br/></td>
<td>Durchsucht einen Pfad nach einem Dateinamen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>Pathfindnextcomponent</strong></a><br/></td>
<td>Analysiert einen Pfad und gibt den Teil dieses Pfads zurück, der dem ersten umgekehrten Schrägstrich folgt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>Pathfindonpath</strong></a><br/></td>
<td>Sucht nach einer Datei.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>Pathfindsuffixarray</strong></a><br/></td>
<td>Bestimmt, ob ein bestimmter Dateiname eine Liste von Suffixen hat.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>Pathgetargs</strong></a><br/></td>
<td>Sucht die Befehlszeilenargumente innerhalb eines angegebenen Pfads.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>Pathgetchartype</strong></a><br/></td>
<td>Bestimmt den Typ des Zeichens im Verhältnis zu einem Pfad.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>Pathgetdrivenumschlag</strong></a><br/></td>
<td>Durchsucht einen Pfad nach einem Laufwerksbuchstaben innerhalb des Bereichs von "a" bis "Z" und gibt die entsprechende Laufwerksnummer zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>Pathiscontenttype</strong></a><br/></td>
<td>Bestimmt, ob der registrierte Inhaltstyp einer Datei mit dem angegebenen Inhaltstyp übereinstimmt. Diese Funktion Ruft den Inhaltstyp für den angegebenen Dateityp ab und vergleicht diese Zeichenfolge mit dem <em>pszcontenttype</em>. Beim Vergleich wird die Groß-/Kleinschreibung nicht berücksichtigt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>Pathisdirectory</strong></a><br/></td>
<td>Überprüft, ob ein Pfad ein gültiges Verzeichnis ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>Pathisdirectoriyempty</strong></a><br/></td>
<td>Bestimmt, ob ein angegebener Pfad ein leeres Verzeichnis ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>Pathisfilespec</strong></a><br/></td>
<td>Durchsucht einen Pfad nach beliebigen Pfad Begrenzungs Zeichen (z. b. ': ' oder ' \' ) '. Wenn keine Pfad Trennzeichen vorhanden sind, wird der Pfad als dateispezifikations Pfad betrachtet.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>"Pthishtmlfile"</strong></a><br/></td>
<td>Bestimmt, ob eine Datei eine HTML-Datei ist. Die Bestimmung erfolgt basierend auf dem Inhaltstyp, der für die Dateierweiterung registriert ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>Pathislfnfilespec</strong></a><br/></td>
<td>Bestimmt, ob ein Dateiname im langen Format vorliegt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>Pathisnetworkpath</strong></a><br/></td>
<td>Bestimmt, ob eine Pfad Zeichenfolge eine Netzwerkressource darstellt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>"Pthistreufix"</strong></a><br/></td>
<td>Durchsucht einen Pfad, um zu bestimmen, ob er ein gültiges Präfix des von <em>pszprefix</em>weiter gegebenen Typs enthält. Ein Präfix ist einer der folgenden Typen: &quot; C: \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>Pathisrelative</strong></a><br/></td>
<td>Durchsucht einen Pfad und bestimmt, ob er relativ ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>Pathisroot</strong></a><br/></td>
<td>Bestimmt, ob eine Pfad Zeichenfolge auf den Stamm eines Volumes verweist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>"Pthissameroot"</strong></a><br/></td>
<td>Vergleicht zwei Pfade, um zu bestimmen, ob Sie eine gemeinsame Stamm Komponente aufweisen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>Ordner "Ordner"</strong></a><br/></td>
<td>Bestimmt, ob ein vorhandener Ordner die Attribute enthält, die ihn zu einem Systemordner machen. Alternativ gibt diese Funktion an, ob bestimmte Attribute einen Ordner als Systemordner qualifizieren.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a><br/></td>
<td>Bestimmt, ob eine Pfad Zeichenfolge ein gültiger Universal Naming Convention (UNC)-Pfad ist, im Gegensatz zu einem Pfad, der auf einem Laufwerk Buchstaben basiert.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>Pathisuncserver</strong></a><br/></td>
<td>Bestimmt, ob eine Zeichenfolge eine gültige UNC-Datei für einen Serverpfad ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>Pathisuncservershare</strong></a><br/></td>
<td>Bestimmt, ob eine Zeichenfolge ein gültiger UNC-Freigabe Pfad ( \\ <em>Server</em> \ <em>Freigabe</em>) ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>Pathisurl</strong></a><br/></td>
<td>Testet eine angegebene Zeichenfolge, um zu bestimmen, ob Sie einem gültigen URL-Format entspricht.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>Pathmakepretty</strong></a><br/></td>
<td>Konvertiert einen Großbuchstaben Pfad in alle Kleinbuchstaben, um dem Pfad eine konsistente Darstellung zu übergeben.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>Pathmakesystemordner</strong></a><br/></td>
<td>Gibt einem vorhandenen Ordner die richtigen Attribute, die zu einem Systemordner werden.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a><br/></td>
<td>Durchsucht eine Zeichenfolge mit einem Platzhalter-Übereinstimmungs Typ.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>Pathmatchspecex</strong></a><br/></td>
<td>Entspricht einem Dateinamen aus einem Pfad mit einem oder mehreren Dateinamen Mustern.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>Pathparametenconlocation</strong></a><br/></td>
<td>Analysiert eine Datei Speicherort Zeichenfolge, die einen Datei Speicherort und einen Symbol Index enthält, und gibt separate Werte zurück.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>Pathquotespaces</strong></a><br/></td>
<td>Durchsucht einen Pfad nach Leerzeichen. Wenn Leerzeichen gefunden werden, wird der gesamte Pfad in Anführungszeichen eingeschlossen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>Pathrelativepathto</strong></a><br/></td>
<td>Erstellt einen relativen Pfad von einer Datei oder einem Ordner zu einem anderen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>"Pthremuveargs"</strong></a><br/></td>
<td>Entfernt alle Argumente aus einem angegebenen Pfad.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>Umgekehrter Schrägstrich</strong></a><br/></td>
<td>Entfernt den nachfolgenden umgekehrten Schrägstrich aus einem angegebenen Pfad.<br/>
<blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Es wird empfohlen, die Funktion <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>pathcchremovebackschräg Strich</strong></a> oder <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>pathcchremovebackslashex</strong></a> zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>"Pthremuveblank"</strong></a><br/></td>
<td>Entfernt alle führenden und nachfolgenden Leerzeichen aus einer Zeichenfolge.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>"Pthremuveextension"</strong></a><br/></td>
<td>Entfernt die Dateinamenerweiterung aus einem Pfad, sofern vorhanden. <br/>
<blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Wir empfehlen die Verwendung von <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>pathcchremoveextension</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>"Pthremuvefilespec"</strong></a><br/></td>
<td>Entfernt den nachfolgenden Dateinamen und den umgekehrten Schrägstrich aus einem Pfad, sofern diese vorhanden sind.<br/>
<blockquote>
[!Note]<br />
Diese Funktion ist als veraltet markiert. Wir empfehlen die Verwendung der <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>pathcchremovefilespec</strong></a> -Funktion an dieser Stelle.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>Pathrenameextension</strong></a><br/></td>
<td>Ersetzt die Erweiterung eines Datei namens durch eine neue Erweiterung. Wenn der Dateiname keine Erweiterung enthält, wird die Erweiterung an das Ende der Zeichenfolge angefügt.<br/>
<blockquote>
[!Note]<br />
Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>pathcchrenrenameextension</strong></a> " zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>Pathsearchandqualify</strong></a><br/></td>
<td>Bestimmt, ob ein angegebener Pfad ordnungsgemäß formatiert und voll qualifiziert ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>Pathsetdlgitempath</strong></a><br/></td>
<td>Legt den Text eines untergeordneten Steuer Elements in einem Fenster oder Dialogfeld fest. dabei wird <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>pathcompactpath</strong></a> verwendet, um sicherzustellen, dass der Pfad in das Steuerelement passt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>Pathskiproot</strong></a><br/></td>
<td>Ruft einen Zeiger auf das erste Zeichen in einem Pfad ab, der auf die Elemente Laufwerk Buchstabe oder UNC-Server/Freigabe Pfad folgt.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>Pathstrippath</strong></a><br/></td>
<td>Entfernt den Pfadteil eines voll qualifizierten Pfads und einer Datei.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>Pathstriptor</strong></a><br/></td>
<td>Entfernt alle Datei-und Verzeichnis Elemente in einem Pfad außer den Stamm Informationen.<br/>
<blockquote>
[!Note]<br />
Der Missbrauch dieser Funktion kann zu einem Pufferüberlauf führen. Es wird empfohlen, die Funktion "sicherere <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>pathcchstriptoroot</strong></a> " zu verwenden.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>Pathundekorieren</strong></a><br/></td>
<td>Entfernt die Dekoration aus einer Pfad Zeichenfolge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>Pathunexpandenvstrings</strong></a><br/></td>
<td>Ersetzt bestimmte Ordnernamen in einem voll qualifizierten Pfad durch die zugehörige Umgebungs Zeichenfolge.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>Ordner "pathunmakesystem"</strong></a><br/></td>
<td>Entfernt die Attribute aus einem Ordner, in dem Sie einen Systemordner bilden. Dieser Ordner muss tatsächlich im Dateisystem vorhanden sein.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>Pathunquotespaces</strong></a><br/></td>
<td>Entfernt Anführungszeichen am Anfang und Ende eines Pfads.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>Shskipconnection</strong></a><br/></td>
<td>Überprüft einen Bindungs Kontext, um festzustellen, ob es sicher ist, eine Bindung an ein bestimmtes Komponenten Objekt herzustellen.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>Urlapplyscheme</strong></a><br/></td>
<td>Bestimmt ein Schema für eine angegebene URL-Zeichenfolge und gibt eine Zeichenfolge mit einem entsprechenden Präfix zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a><br/></td>
<td>Konvertiert eine URL-Zeichenfolge in ein kanonisches Format.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>Urlcombine</strong></a><br/></td>
<td>Wenn eine relative URL und deren Basis bereitgestellt wird, wird eine URL in kanonischer Form zurückgegeben.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>Urlcompare</strong></a><br/></td>
<td>Berücksichtigt den Vergleich von zwei URL-Zeichen folgen in Groß-und Kleinschreibung.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>Urlkreatefrompath</strong></a><br/></td>
<td>Konvertiert einen MS-DOS-Pfad in eine kanonisierte URL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>Urlescape</strong></a><br/></td>
<td>Konvertiert Zeichen oder Ersatz Zeichenpaare in eine URL, die möglicherweise während des Transports über das Internet ( &quot; Unsichere Zeichen) in die entsprechenden Escapesequenzen geändert wird &quot; . Ersatz Zeichenpaare sind Zeichen zwischen u + 10000 und U + 10FFFF (in UTF-32) oder zwischen DC00 und und DFFF (in UTF-16). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>Urlescapespaces</strong></a><br/></td>
<td>Ein Makro, das Leerzeichen in die entsprechende Escapesequenz konvertiert.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>Urlgetlocation</strong></a><br/></td>
<td>Ruft den Speicherort von einer URL ab.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>Urlgetpart</strong></a><br/></td>
<td>Akzeptiert eine URL-Zeichenfolge und gibt einen angegebenen Teil dieser URL zurück.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>Urlhash</strong></a><br/></td>
<td>Hashes einer URL-Zeichenfolge.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a><br/></td>
<td>Testet, ob eine URL ein angegebener Typ ist.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>Urlisfileurl</strong></a><br/></td>
<td>Testet eine URL, um zu bestimmen, ob es sich um eine Datei-URL handelt.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>Urlisnohistory</strong></a><br/></td>
<td>Gibt zurück, ob eine URL eine URL ist, die Browser in der Regel nicht in den Navigationsverlauf einschließen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>Urlisopaque</strong></a><br/></td>
<td>Gibt zurück, ob eine URL nicht transparent ist.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>Urlunescape</strong></a><br/></td>
<td>Konvertiert Escapesequenzen zurück in normale Zeichen.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>Urlunescapanplace</strong></a><br/></td>
<td>Konvertiert Escapesequenzen zurück in normale Zeichen und überschreibt die Original Zeichenfolge.<br/></td>
</tr>
</tbody>
</table>



 

 

 




